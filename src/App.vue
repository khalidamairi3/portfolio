<template>
  <div id="app">
    <pageHeader />
    <router-view />
  </div>
</template>
<script>
import pageHeader from "./components/header"

export default {
  components: {
    pageHeader,
  },
  data() {
    return {
      shown: true
    }
  },
  
}


</script>ipt

<style>
@import url('https://fonts.googleapis.com/css2?family=Fjalla+One&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Old+Standard+TT&display=swap');
@import url("https://use.fontawesome.com/releases/v5.15.0/css/all.css");
@import url("https://use.fontawesome.com/releases/v5.15.0/css/v4-shims.css");
#app {
  margin: 0;
  padding: 0;
  /* font-family: Avenir, Helvetica, Arial, sans-serif; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;


}
body{
  font-family: 'Fjalla One', sans-serif;
  margin: 0;
  padding: 0;
}
.shown{
    display: grid;
    grid-template-columns: 1fr 3fr;

}

button{
  cursor: pointer;
}

.hidden{
  display: none;
}
#nav {
  display: none;
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
