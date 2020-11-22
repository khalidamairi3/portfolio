<template>
    <div id="contact">
        <h1 id="contact-header"> Contact </h1>
        <i class="fas fa-map-marker-alt fa-2x" style="color:white"> <span class="icon-span"> Edmonton,AB Canada </span> </i>
         <a class="icon-span" href="mailto:khalidamairi3@gmail.com"><i class="far fa-envelope-open fa-2x" style="color:white"> </i> khalidamairi3@gmail.com </a> 
         <a class="icon-span" href="tel:+15875684533"> <i class="fas fa-phone-square-alt fa-2x" style="color:white"> </i> +1 587-568-4533 </a>
        <a class="icon-span" target="_blank" href="https://www.linkedin.com/in/khaled-amayri/"> <i class="fab fa-linkedin fa-2x" style="color:white"></i> LinkedIn Profile  </a>
        <a class="icon-span" target="_blank" href="https://github.com/khalidamairi3"> <i class="fab fa-github fa-2x" style="color:white"></i> Github Profile  </a>
        

    </div>
</template>

<script>
    export default {
        name:"page-contact"
    }
</script>

<style scoped>

#contact{
    text-align: center;
    padding: 5%;
    width: 100%;
    counter-reset: white;
    display: grid;
    align-items: center;
    justify-items: center;
    row-gap: 4vh;
    background-color: black ;
    padding-bottom: 10vh;

}

.icon-span{
    font-family: 'Fjalla One', sans-serif;
    font-size: 18px;
    color: white;
    text-decoration: none;
    font-weight: normal;
}
#contact-header{
    grid-column: 1/-1;
    color: white;
    width: 50%;
    border-bottom: 2px solid;
}

</style>