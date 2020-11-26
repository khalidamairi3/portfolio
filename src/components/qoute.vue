<template>
    <div id="qoute">
        <h1 id="qoute-header"> Get a Qoute </h1>
        <label for="name"> Name: </label>
        <input type="text" name="name" v-model="name">
        <label for="email"> Email:</label>
        <input name="email" type="text" v-model="email">
        <label for="description"> Message: </label>
        <textarea name="description" id="text" v-model="text" ></textarea>

        <button :disabled = disable @click="postqoute()"> Submit </button>

        <p style="grid-column: 1/-1" v-if="submited"> Thank you, we will get back to you soon </p>
        <p v-if="err"> Couldn't submit the qoute </p>


    </div>
</template>

<script>
import axios from "axios"
    export default {
        name:"qoute-section",
        data() {
            return {
                name:"",
                email: "",
                text:"",
                submited:false,
                disable:false,
                err:false

            }
        },
        methods: {
            postqoute() {
                this.disable = true;
                axios.request({
                    url: "http://127.0.0.1:5000/api/qoute",
                    method: "POST",
                    data:{
                        "email":this.email,
                        "name":this.name,
                        "message":this.text
                    }
                }).then(()=>{
                    this.disable=false;
                    this.submited=true;
                    this.name="";
                    this.email="";
                    this.text="";
                }).catch(()=>{
                    this.disable=false;
                    this.err=true;
                    
                })
                
            }
        },
    }

</script>

<style scoped>
#qoute{
    width: 100%;
    display: grid;
    align-items: center;
    justify-items: center;
    border :10px solid #fca311;
    background-color:#14213d ;
    color:white ;
    grid-template-columns: 2fr 4fr;
    row-gap: 5vh;
    padding-bottom: 5vh;
}
label{
    justify-self: end;
}
#qoute-header{
    grid-column: 1/-1;
    border-bottom: 2px solid;
    padding-bottom: 10px;
}

input{
    width: 80%;
    border: 2px solid #fca311;
    height: 5vh;
    
}
button{
    font-size: 1.5em;
    grid-column: 1/-1;
    border: 2px solid;
    color: white;
    background: #fca311;
    padding: 15px;
    transition: all ease-in 0.5s;
}

button:hover{
    
    color: #fca311;
    background:white;
    padding: 15px;
}
label{
    font-size: 1.5em;
}

textarea{
    width: 80%;
    height: 30vh;
    border: 2px solid #fca311;
}
</style>