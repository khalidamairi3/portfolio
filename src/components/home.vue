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
                <p> I'm fresh, attentive, and detailed orientated Computer Engineer with Full-Stack Developer background and excellent communication skills. Studying computer engineering made me highly knowledgable in various programming languages with superior problem-solving skills which i deployed recently in Innotech college Full Stack program to graduate with <strong>100%</strong> score. My passion for web development took me further to learn more about relevant fields such as cloud computing services with aws, data science, IOT and digital marketing. My goal is to be able to combine data science with web development to create impressive apps that would provide precise solutions to different kind of problems  </p>
           
                </div>
                <div id="about-image">
                    <img src="../assets/khaled.jpeg" alt="">
                </div>
        </div>
        <projectsPage/>
        <skillSet />
        <qouteSection />
        <contacPage />
        
    </div>
</template>

<script>
import qouteSection from "./qoute"
import contacPage from "./contact";
import skillSet from "./skillSet";
import projectsPage from "./projects"; 
    export default {
        name: "home-page",
        components: {
            projectsPage,
            skillSet,
            contacPage,
            qouteSection
        },
       
    }
</script>

<style  scoped>

@media only screen and (min-width: 1000px ) {

    #home-content{
    position: absolute;
    bottom: 40vh;
    right: 30vw;
    font-size: 2rem;
    letter-spacing: 0.2rem;
    
    
}
    
}

#home{
    display: grid;
    justify-items: center;
    align-items: center;
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
    bottom: 60vh;
    right: 5vw;
    font-size: 1.5rem;
    letter-spacing: 0.2rem;
    color: white;
    width: 100%;
    
    
}

#text {
    position: relative;
    left: 5vw;
    top: 30vh
    
}
#about{
    margin-top:-0.5% ;
    background-color: #14213d; 
    width: 100%;
    display: grid;
    color: white;
    justify-items: center;
    align-items: center;
    /* grid-template-columns: minmax(350px,1fr) ; */
}
#about-header{
    /* grid-column: span 2; */
    width: 30%;
    border-bottom: 2px solid white;
    letter-spacing: 0.2rem;
    padding: 10px;
}

#about-content{
    width: 100%;
    display: grid;
    justify-items: center;
    align-items: center;

    
}
#about-image{
    width: 80%;
}
#about-image img{
    
    height: 60vh;
    border-radius: 15px 15px 15px 15px;
    margin-bottom: 5vh;
    transition: none;

    
}

#about-image img:hover{
    width: 100%;
}
p{
    width: 80%;
    font-size: 1.2em;
    text-align: justify;
}
</style>