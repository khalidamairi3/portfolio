<template>
    <div id="skillset">
        <div id="skillset-header">

            <!-- <img src="https://st2.depositphotos.com/1803840/6857/v/600/depositphotos_68579803-stock-illustration-gears-inside-brain.jpg" alt=""> -->
            <h1 id="skillset-header-text" > Skills </h1>
            </div>

            <div class="skill">
                <div class="skill-header">
                    <img src="https://cdn.dribbble.com/users/150679/screenshots/5481730/weiching.jpg" alt="">
                    <h3> Frontend Skills </h3>
                </div>
                <i class="fab fa-html5 fa-5x" style="color : #e34c26"></i>
                <i class="fab fa-css3-alt fa-5x" style="color : #264de4"></i>
                <i class="fab fa-js-square fa-5x" style="color : #323330"></i>
                <i class="fab fa-sass fa-5x" style="color : #cc6699"></i>
                <i class="fab fa-vuejs fa-5x" style="color : #42b883"></i>
                <i class="fab fa-react fa-5x" style="color : #61dbfb"></i>
                
               
                
                
                

            
            <div class="skill"></div>
            <div class="skill"></div>
        </div>



    </div>
</template>

<script>
    export default {
        name:"skill-set"
        
    }
</script>

<style scoped>
#skillset{
    width: 100%;
    display: grid;
    align-items: center;
    justify-items: center;
    background-color:#e5e5e5 ;
    z-index: 5;
    grid-template-columns: minmax(300px,1fr);
}

#skillset-header {
    width: 100%;
    display: grid;
    align-items: center;
    justify-items: center;

    
}

#skillset-header-text{
    grid-column: 1/-1;
    padding-bottom: 10px;
    width: 40%;
    border-bottom: 2px solid ;
}
.skill{
    width: 100%;
    display: grid;
    grid-template-columns: repeat(3,1fr);
    row-gap: 5vh;
    column-gap: 2vw;
}
.skill-header img {

    width: 40vw;
    height: 25vh;
    object-fit: cover;
    border-radius: 15px;

}

.skill-header{
    grid-column: 1/-1;
}
</style>