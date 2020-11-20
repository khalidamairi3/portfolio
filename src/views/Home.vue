<template>
   <div>

        <homePage />

    </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import homePage from "../components/home"
export default {
  name: "Home",
  components: {
    homePage
    // HelloWorld
  }
};
</script>
