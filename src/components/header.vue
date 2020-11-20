<template>
    <div id="header">
        <router-link to="/">KHALED AMAYRI</router-link>
        <div></div> 
        <router-link to="/about">About</router-link>
        <router-link to="/projects">Projects </router-link> 


    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
#header{
    padding: 30px;
    background-color: #FCA311;
    display: none;
    grid-template-columns: 4fr 6fr 1fr 1fr;
    column-gap: 5vw;
}
a{
    color:#FFFFFF;
    text-decoration: none;
    font-size: 24px;
    letter-spacing: 0.1rem;
}

a:hover {

    color:#14213D;



}

</style>