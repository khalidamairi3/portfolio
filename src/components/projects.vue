<template>
  <div id="projects">
    <h1 id="projects-header">Projects</h1>
    <projectItem
      v-for="project in projects"
      :key="project.title"
      :project="project"
    />
  </div>
</template>

<script>
import projectItem from "./project";
export default {
  name: "projects-page",
  components: {
    projectItem,
  },
  data() {
    return {
      projects: [
        {
          title: "Covid Tracker",
          description:
            "Simple covid Tracking app to show and visualize covid data for all countries around the world. The app is implemented using Vue, Vuetify ,chart.js for graphs and external api to retrieve data from",
          code: "https://github.com/khalidamairi3/covid-tracking",
          link: "https://covidtracking.ml/",
          image:
            "https://images.unsplash.com/photo-1584036561566-baf8f5f1b144?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1032&q=80",
        },

        {
          title: "KhaledClasses front-end",
          description:
            "Classes system that provide a modern education system where instructors can view their courses and students, add tasks, view tasks' submissions and grade them. Students can view their courses and tasks in order to submit their solution. All users and courses are managed by admin user",
          code: "https://github.com/khalidamairi3/MVP_frontend.git",
          link: "https://khaledclasses.ml/#/",
          image:
            "https://www.gethow.org/wp-content/uploads/2014/01/classes.jpg",
        },

        {
          title: "KhaledClasses back-end",
          description:
            "API impelementation for khaledClasses project that talks with SQL database and serve more than 20 functionalities",
          code: "https://github.com/khalidamairi3/MVP_backend.git",
          link: false,
          image:
            "https://www.danielleskosky.com/wp-content/uploads/media-uploads/what-is-an-api/xapi-with-outlets.jpg.pagespeed.ic.O5eAY5eU_M.webp",
        },
        {
          title: "Tweeter front-end",
          description:
            "CRUD responsive tweeter website project implemented using Vue.js communicating with API and hosted on google cloud",
          code: "https://github.com/khalidamairi3/vueTweeter.git",
          link: "https://tweeeter.ml/#/",
          image:
            "https://cdn.dribbble.com/users/21059/screenshots/643154/tweet-count.png",
        },

        {
          title: "Tweeter back-end",
          description:
            "API impelementation for tweeter project that talks with SQL database and serve more than 20 functionalities",
          code: "https://github.com/khalidamairi3/tweeter_backend.git",
          link: false,
          image:
            "https://www.danielleskosky.com/wp-content/uploads/media-uploads/what-is-an-api/xapi-with-outlets.jpg.pagespeed.ic.O5eAY5eU_M.webp",
        },

        {
          title: "Okotoks-pizza",
          description:
            "Restaurant responsive website project implemented with pure HTML and CSS (SASS)",
          code: "https://github.com/khalidamairi3/Okotoks.git",
          link: "https://okotoks-pizza.ml/",
          image:
            "https://images.unsplash.com/photo-1513104890138-7c749659a591?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxleHBsb3JlLWZlZWR8MXx8fGVufDB8fHx8&w=1000&q=80",
        },
        {
          title: "Blog Post App",
          description:
            "CRUD blog post website that allows users to sign up and create an account. Login/logout functionality, create a post, delete a post, remove or approve comments, markdown and syntax highlighting to posts. Implemented using Django, Bootstrap, HTML, CSS, JavaScript and Python",
          code: "https://github.com/khalidamairi3/django_blog_app.git",
          link: "https://blog-post-django-app.herokuapp.com/",
          image:
            "https://blog.tubikstudio.com/wp-content/uploads/2016/08/tubik-studio-logo-branding-design-1024x792.png",
        },
      ],
    };
  },
};
</script>

<style scoped>
#projects {
  width: 90%;
  column-gap: 3vw;
  padding-top: 5vh;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  justify-items: center;
  align-items: center;
  color: #fca311;
}

#projects-header {
  padding: 10px;
  grid-column: 1/-1;
  width: 40%;
  border-bottom: 2px solid;
  letter-spacing: 0.2rem;
}
</style>
