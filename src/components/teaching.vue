<template>
    <div id="teaching">
        <h1 id="teaching-header"> Tutoring </h1>
        <div id="teaching-content">
            <p> 
                 Teaching is one of my passions! I believe that the ability to teach demonstrates the highest form of understanding and it creates a positive bond of communication. I have always appreciated the value that I can add to students as much as the knowledge I gain by teaching. What started as a passion took a professional leap when I was selected to be a Student Assistant in one of the programming courses at Middle East Technical University. Completing my studies and teaching simultaneously allowed me to fully understand what might a student be struggling with and made my help most significant.  I am also leading weekly study sessions for other developers where I offer practice problems and group-debugging over a virtual platform          
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