<template>
    <div id="skillset">
        <div id="skillset-header">

            <!-- <img src="https://st2.depositphotos.com/1803840/6857/v/600/depositphotos_68579803-stock-illustration-gears-inside-brain.jpg" alt=""> -->
            <h1 id="skillset-header-text" > Skills </h1>
            </div>

            <div class="skill">
                <div class="skill-header">
                    <img src="https://www.flaticon.com/svg/static/icons/svg/2166/2166822.svg" alt="">
                    <h3> Frontend Skills </h3>
                </div>
                <i class="fab fa-html5 fa-5x" style="color : #e34c26"></i>
                <i class="fab fa-css3-alt fa-5x" style="color : #264de4"></i>
                <i class="fab fa-js-square fa-5x" style="color : #323330"></i>
                <i class="fab fa-sass fa-5x" style="color : #cc6699"></i>
                <i class="fab fa-vuejs fa-5x" style="color : #42b883"></i>
                <i class="fab fa-react fa-5x" style="color : #61dbfb"></i>
                <i class="fab fa-bootstrap fa-5x" style="color : #563d7c"></i>
                
                
            </div>

            <div class="skill">

                <div class="skill-header">
                    <img src="https://cdn.iconscout.com/icon/premium/png-512-thumb/backend-website-1878750-1592883.png" alt="">
                    <h3> Backend Skills </h3>
                </div>
                <img src="https://image.flaticon.com/icons/png/512/29/29165.png" width="80px" alt="">
                <img src="https://img.pngio.com/logo-mongodb-png-transparent-logo-mongodbpng-images-pluspng-mongodb-png-413_484.png" width="80px" alt="">
                <i class="fab fa-node-js fa-5x" style="color : #68a063"></i>
                <img src="https://vectorified.com/images/express-js-icon-10.png" width="80px" alt="">
                <i class="fab fa-php fa-5x" style="color : #787cb5"></i>
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/1200px-Python-logo-notext.svg.png" width="80px" alt="">
                <img src="https://cdn.freebiesupply.com/logos/thumbs/2x/flask-logo.png"  width="80px" alt="">
                <img src="https://cdn.iconscout.com/icon/free/png-512/django-2-282855.png" width="80x" alt="">
                <img src="https://cdn.iconscout.com/icon/free/png-256/java-25-226002.png" width="80px" alt="">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/93/Amazon_Web_Services_Logo.svg/1280px-Amazon_Web_Services_Logo.svg.png" width="80px" alt="">
                <img src="https://cdn.iconscout.com/icon/premium/png-512-thumb/api-1675146-1421517.png" width="80x" alt="">

            </div>
            <div class="skill">  
                <div class="skill-header">
                    <img src="https://cdn3.iconfinder.com/data/icons/innovation-technology/68/15-512.png" alt="">
                    <h3> Relevant Skills </h3>
                </div>
                <img src="https://cdn.iconscout.com/icon/free/png-512/c-programming-569564.png" width="80px" alt="">
                <img src="https://images.vexels.com/media/users/3/166253/isolated/preview/14bc03b7b1c2c4e2656fd4c0a981cbbc-cpp-programming-language-icon-by-vexels.png"  width="80px" alt="">
                <i class="fab fa-git-alt fa-5x" style="color : #f34f29">  </i>
                <i class="fab fa-github fa-5x" style="color : #211f1f"></i>
                <img src="https://cdn4.iconfinder.com/data/icons/technology-83/1000/object_programming_development_oriented_developer_object-oriented_programming_software-512.png" width="80px" alt="">
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
    row-gap: 5vh;
    padding-bottom: 10vh;

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
    align-items: center;
    justify-items: center;
    row-gap: 5vh;
    column-gap: 2vw;
    
}
.skill-header img {

    width: 45vw;
    height: 25vh;
    object-fit: cover;
    border-radius: 15px;

}

.skill-header{
    grid-column: 1/-1;
}
</style>