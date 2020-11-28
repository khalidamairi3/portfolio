<template>
    <div id="review-form" data-aos="zoom-in-right" data-aos-duration ="1000">

    <label for="name"> Name: </label>
    <input type="text" name="name" v-model="name">
    <label for="email"> Email: </label>
    <input type="text" v-model="email">
    <label for="review"> Review: </label>
    <textarea v-model="text" ></textarea>
    <label> Rate: </label>

    <ul  class="rating">
    <li @click="reviewCheck(1)" class="star rating-item" data-rate="1"></li>
    <li @click="reviewCheck(2)" class="star rating-item" data-rate="2"></li>
    <li @click="reviewCheck(3)" class="star rating-item active" data-rate="3"></li>
    <li @click="reviewCheck(4)" class="star rating-item" data-rate="4"></li>
    <li @click="reviewCheck(5)" class="star rating-item" data-rate="5"></li>
    </ul>
    <button @click="postReview()" type="submit"> Submit </button>
    </div>
</template>

<script>
import axios from "axios";
    export default {
        name:"review-form",
        data() {
            return {
                rate : 3,
                name:"",
                email:"",
                text:""
            }
        },
        methods: {
            reviewCheck(index){

                let stars = document.querySelectorAll(".star")
                stars.forEach(element => {
                    element.classList.remove("active")
                    
                });

                stars[index-1].classList.add("active");
                this.rate = index;
                

                
            },
            postReview(){
                axios.request({
                    url:"https://khaledamayri.com/api/reviews",
                    method:"POST",
                    data:{
                        "name":this.name,
                        "email":this.email,
                        "message":this.text,
                        "rate":this.rate
                    }

                }).then(()=>{ 
                    let data={
                        "id":100,
                        "name":this.name,
                        "email":this.email,
                        "message":this.text,
                        "rate":this.rate
                    }
                    console.log(data);
                    this.$emit("addReview",data)
                }).catch(()=>{})

            }
        },
    }
</script>

<style scoped>

label{
    justify-self: end;
    font-family: 'Old Standard TT', serif;
}
#review-form{
    min-width: 35%;
    grid-column: 1/-1;
    max-width: 800px;
    row-gap: 2vh;
    display: grid;
    grid-template-columns: 1fr 2fr;
    border: 2px solid black;
    border-radius: 10px;
    margin: 8vh 2vw;
    padding: 3vh 2vw;
}
textarea{
    height: 15vh;
}

.rating {
width: fit-content;
display: flex;
padding: 0;
margin: 0;
}

.rating li {
list-style-type: none
}

.rating-item {
border: 1px solid #fff;
cursor: pointer;
font-size:2em;
color: #fca311;
}

/* initial: make all stars full */
.rating-item::before {
content: "\2605";
}

/* make until the clicked star (the rest) empty */
.rating-item.active ~ .rating-item::before {
content: "\2606";
}

/* on hover make all full */
.rating:hover .rating-item::before {
content: "\2605";
}

/* make until the hovered (the rest) empty */
.rating-item:hover ~ .rating-item::before {
content: "\2606";
}

button{
    width: 50%;
    grid-column: 1/-1;
    border: 2px solid;
    color: white;
    background: #fca311;
    padding: 5px;
    transition: all ease-in 0.5s;
    justify-self: center;
}

button:hover{
    
    color: #fca311;
    background:white;
    /* padding: 15px; */
}

</style>