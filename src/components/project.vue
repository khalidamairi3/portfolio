<template>
  <div class="project" data-aos="zoom-in" data-aos-duration="1000">
    <img :src="project.image" alt="" />
    <h3 class="project-header">{{ project.title }}</h3>
    <p>{{ project.description }}</p>
    <div class="options">
      <a :href="project.code" target="_blank">
        <button><i class="fas fa-code-branch"></i> Code</button></a
      >
      <a v-if="project.link" :href="project.link" target="_blank">
        <button><i class="fas fa-eye"></i> Live</button></a
      >
    </div>
  </div>
</template>

<script>
export default {
  name: "project-item",
  props: {
    project: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.project {
  display: grid;
  justify-items: center;
  align-items: center;
  width: 85%;
  overflow: hidden;
  border-radius: 15px;
  background-color: white;
  color: black;
  margin-bottom: 5vh;
}

.project-header {
  color: #fca311;
  width: 50%;
  border-bottom: 2px solid;
}
p {
  font-family: "Old Standard TT", serif;
  text-align: justify;
  font-size: 1.2em;
}
button {
  padding: 15px;
  background-color: white;
  color: #fca311;
  border: none;
  font-size: 1.2em;
  margin-bottom: 2vh;
  border-radius: 10px;
  cursor: pointer;
  transition: all ease-in 0.5s;
}
button:hover {
  background-color: #fca311;
  color: white;
  border: none;
}

img {
  height: 30vh;
  width: 100%;
  object-fit: cover;
}

.options {
  display: grid;
  grid-template-columns: 1fr 1fr;
  column-gap: 2vw;
  align-items: center;
  justify-items: flex-start;
}
a {
  color: #fca311;
  text-decoration: none;
}
</style>
