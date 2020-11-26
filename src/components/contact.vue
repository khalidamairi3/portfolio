<template>
  <div id="contact">
    <h1 id="contact-header">Contact</h1>

    <div>
        <i class="fas fa-map-marker-alt fa-2x" style="color: white">
        <span class="icon-span"> Edmonton,AB Canada </span>
      </i>
      <a class="icon-span" href="mailto:khalidamairi3@gmail.com"
        ><i class="far fa-envelope-open fa-2x" style="color: white"> </i>
        khalidamairi3@gmail.com
      </a>
      <a class="icon-span" href="tel:+15875684533">
        <i class="fas fa-phone-square-alt fa-2x" style="color: white"> </i> +1
        587-568-4533
      </a>

    </div>

    <div>
         <a
        class="icon-span"
        target="_blank"
        href="https://www.linkedin.com/in/khaled-amayri/"
      >
        <i class="fab fa-linkedin fa-2x" style="color: white"></i> LinkedIn
        Profile
      </a>

      <a
        class="icon-span"
        target="_blank"
        href="https://github.com/khalidamairi3"
      >
        <i class="fab fa-github fa-2x" style="color: white"></i> Github Profile
      </a>

    </div>
      
    
    
     
    
  </div>
</template>

<script>
export default {
  name: "page-contact",
};
</script>

<style scoped>
#contact, #contact div {
  text-align: justify;
  width: 100%;
  counter-reset: white;
  display: grid;
  align-items: center;
  justify-items: center;
  row-gap: 4vh;
  background-color: black;

}

#contact{
    padding: 10%;
    
}

.icon-span {
  font-family: "Fjalla One", sans-serif;
  font-size: 18px;
  color: white;
  text-decoration: none;
  font-weight: normal;
}
#contact-header {
    text-align: center;
  grid-column: 1/-1;
  color: white;
  width: 50%;
  border-bottom: 2px solid;
}
@media only screen and (min-width: 1000px) {
  #contact {
    grid-template-columns: 1fr 1fr;
    padding: 5%;
  }
}
</style>