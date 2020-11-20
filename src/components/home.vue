<template>
    <div id="home">
        <img src="../assets/home4.jpg" alt="" >
        <div id="home-content">
           <h2> KHALED AMAYRI  </h2>
           <h3 id="text"> COMPUTER ENGINEER & FULLSTACK DEVELOPER</h3>  
        </div>
        <div id="about">
            <h1 id="about-header"> About </h1>
            <div id="about-content">
                <h3> Hello! I'm Khaled </h3>
                <p> I'm fresh, attentive, and detailed orientated Computer Engineer with Full-Stack Developer background and excellent communication skills. Studying computer engineering made me highly knowledgable in various programming languages with superior problem-solving skills which i deployed recently in Innotech college Full Stack program to graduate with <strong>100%</strong> score. My passion for web development took me further to learn more about relevant fields such as cloud computing services with aws, data science, IOT and digital marketing. My goal is to be able to combine data science with web development to create impressive apps that would provide precise solutions to different kind of problems  </p>
           
                </div>
                
        </div>
    </div>
</template>

<script>

    export default {
        name: "home-page",
    }
</script>

<style  scoped>

#home{
    width: 100%;
    overflow: hidden;
}

img{
    width: 100%;
    height: 80vh;
    object-fit:cover;
    opacity: 0.95;
    transition: all ease-in 2s;
    margin: 0;
}

img:hover{
    width: 110%;
    overflow: none;
}

#home-content{
    text-shadow: 3px 5px black;
    margin: 0;
    position: absolute;
    bottom: 40vh;
    right: 30vw;
    font-size: 2rem;
    letter-spacing: 0.2rem;
    color: white;
    width: 100%;
    
    
}

#text {
    position: relative;
    left: 15vw;
    
}
#about{
    margin-top:-0.5% ;
    background-color: #14213d; 
    width: 100%;
    display: grid;
    color: white;
    grid-template-columns: 1fr 1fr ;
}
#about-header{
    grid-column: span 2;
    margin-left:35% ;
    width: 30%;
    border-bottom: 2px solid white;
    letter-spacing: 0.2rem;
}

#about-content{
    width: 100%;
    text-align: center;
    
}
p{
    width: 70%;
    margin-left: 15%;
    font-size: 1.2em;
    text-align: justify;
}
</style>