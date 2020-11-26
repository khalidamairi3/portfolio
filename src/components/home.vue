<template>
    <div id="home">
        <img id="main-image" src="../assets/home4.jpg" alt="" >
        <div id="home-content" data-aos="fade-left" data-aos-duration="3000">
           <h2> KHALED AMAYRI  </h2>
           <h3 id="text"> COMPUTER ENGINEER & FULLSTACK DEVELOPER</h3>  
        </div>
        <div id="about" data-aos="fade-down"  data-aos-duration="2000">
            <h1 id="about-header"> About </h1>
            <div id="about-content" data-aos="fade-right"  data-aos-duration="2000">
                <p> I am a fresh, attentive, and detail-orientated Computer Engineer with Full-Stack Developer background and excellent communication skills. Studying computer engineering made me highly knowledgeable in various programming languages with superior problem-solving skills which I deployed recently in Innotech college Full Stack program to graduate with 100% score. My passion for web development allowed me to learn about relevant fields such as cloud computing services with AWS , data science, IOT and digital marketing. My goal is to be able to combine data science with web development to create impressive apps that would provide precise solutions to different kinds of problems.  </p>
                    <a href="https://drive.google.com/file/d/128cMsOta43spDwyHXm3YAjNWU3yDiZmw/view?usp=sharing" target="_blank"> <button> Resume </button>  </a>          
                </div>
                <div id="about-image" data-aos="fade-left"  data-aos-duration="2000">
                    <img src="../assets/khaled.jpeg" alt="">
                </div>
        </div>
        <projectsPage data-aos="fade-down" data-aos-duration ="100"/>
        <skillSet data-aos="fade-down" data-aos-duration="1000" />
         <teachingSection data-aos="zoom-in-right" data-aos-duration="1000"/>
        <qouteSection />
        <contacPage />
        
    </div>
</template>

<script>
import teachingSection from "./teaching"
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
            qouteSection,
            teachingSection
        },
       
    }
</script>

<style  scoped>

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

}

#main-image{
    opacity: 0.95;
    transition: all ease-in 2s;
    margin: 0;
}

#main-image :hover{
    width: 110%;

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
    padding-bottom: 5vh;
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
    padding-bottom: 5vh;
    font-family: 'Old Standard TT', serif;
    font-size: 1.2em;
    

    
}

#about-content button{
    padding: 15px 25px;
    font-size: 1.2em;
    font-weight:  bold;
    background-color: #fca311;
    border: 2px solid white ;
    color:white;
    transition: all ease 0.5s;
}
#about-content button:hover{
    
    background-color: #14213d;
    color: white;
    border:2px solid #fca311 ;

}


#about-image{
    width: 80%;
}
#about-image img{
    
    height: 60vh;
    border-radius: 15px 15px 15px 15px;
    margin-bottom: 5vh;

    
}

/* #about-image img:hover{
    width: 100%;
} */
p{
    width: 80%;
    font-size: 1.2em;
    text-align: justify;
}

@media only screen and (min-width: 600px ) {
    img{
        height: 80vh;
    }
    #main-image:hover{
        width: 115%;
    }
    #home-content{
    position: absolute;
    bottom: 50vh;
    right: 0vw;
    font-size: 2rem;
    letter-spacing: 0.3rem;

    }

    

    #text {
    position: relative;
    top: 20vh;
    left: 0vw;
    
}





}

@media only screen and (min-width: 1000px ) {

    img{
        height: 100vh;
    }

    #home-content{
    position: absolute;
    bottom: 0;
    right: 25vw;
    font-size: 2rem;
    letter-spacing: 0.2rem;
    
    
}

#text{
    top: 0;
    left: 22vw;
}

#about{

    grid-template-columns: 1fr 1fr;
}
#about-header{
    grid-column: 1/-1;

}

#about-content{
    border-right: 8px solid #fca311;
}
#about-image img{
    height: 50vh;
    width: 90%;
    
}
#about-image img :hover{

    width: 90%;
    
}

    
}




</style>