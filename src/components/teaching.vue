<template>
    <div id="teaching">
        <h1 id="teaching-header"> Tutoring </h1>
        <div id="teaching-content">
            <p> 
                Teaching is one of my favorite hobbies. I enjoy the value i can add to students to learn new skills and get their work done. This hobby took a professional move after I was selected to be a Student Assistant in programming courses during my studies in the university. Being a student and an assistant at the same time gave me the ability to tackle students' points of weakness because as a student i am familiar with the difficulties they might have. Currently, I'm leading weekly study sessions for other developers peers where I offer more practice problems and group debugging for those who need it.          
            </p>

        </div>
        <div id="teaching-image">
            <img src="https://cdn1.iconfinder.com/data/icons/online-business-34/512/tutor-remote-teacher-computer-online-512.png" width="85%" alt="">
        </div>
        <h3 @click="reviews =!reviews" v-if="!reviews" style="cursor : pointer; grid-column:1/-1; "> View reviews
        <img src="https://www.computaris.com/wp-content/uploads/2017/01/arrow.jpg" width="50px" alt="">
         </h3>
        <h3 @click="reviews =!reviews " v-if="reviews" style="cursor : pointer; grid-column:1/-1;"> Hide reviews </h3>
        <reviewsPage v-if="reviews"/>


    </div>
</template>

<script>
import reviewsPage from "./reviews"
    export default {
        name:"teaching-section",
        components: {
            reviewsPage,
        },
        data() {
            return {
                reviews: false
            }
        },
    }
</script>

<style scoped>
#teaching-header{
    width: 40%;
    padding: 10px;
    grid-column:1/-1 ;
    border-bottom: 1px solid #14213d;
}
#teaching-content{
    align-self: baseline;
    width: 80%;
    font-size: 1.5em;
    font-family: 'Old Standard TT', serif;
    text-align: justify;
}
#teaching{
    display: grid;
    align-items: center;
    justify-items: center;
    color: #14213d;

}

@media only screen and (min-width: 1000px) {
    #teaching{
            grid-template-columns: 3fr 2fr;
    }
    
}

</style>