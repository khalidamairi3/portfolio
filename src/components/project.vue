<template>
    <div class="project">

        <img :src="project.image" alt="">
        <h3 class="project-header"> {{project.title}} </h3>
        <p> {{project.description }}</p>
        <div class="options">
           <a :href=" project.code" target="_blank"> <button> <i class="fas fa-code-branch"></i> Code </button></a> 

           
           <a v-if="project.link" :href="project.link" target="_blank">  <button> <i class="fas fa-eye"></i> Live</button></a>
           
            

        </div>
        
    </div>
</template>

<script>
    export default {
        name:"project-item",
        props: {
            project: {
                type: Object,
                required: true 
            },
        },
    }
    
</script>

<style scoped>

.project{
    display: grid;
    justify-items: center;
    align-items: center;
    width: 85%;
    overflow: hidden;
    border-radius: 15px;
    background-color:white ;
    color: #fca311;
    margin-bottom: 5vh;

}

.project-header{
    width: 50%;
    border-bottom: 2px solid;
}
p{
    text-align: justify;

}
button{
    padding: 10px;
    background-color: #fca311;
    color: white;
    border: none;
    font-size:1.2em;
    margin-bottom: 2vh ;
    border-radius:15px ;
}

img{
    height: 30vh;
    width: 100%;
    object-fit: cover;
}

.options{
    display: grid;
    grid-template-columns: 1fr 1fr;
    column-gap: 10vw;
}
a{
    color:#fca311 ;
    text-decoration: none;
}

</style>