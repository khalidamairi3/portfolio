<template>
    <div  id="projects">
        <h1 id="projects-header"> Projects </h1>
        <projectItem v-for="project in projects" :key="project.title"  :project = project />

    </div>
</template>

<script>
import projectItem from "./project";
    export default {
        name:"projects-page",
        components: {
            projectItem,
        },
         data() {
            return {
                projects: [ 
                    { 
                    "title" : "Tweeter front-end" ,
                    "description" : "CRUD responsive tweeter website project implemented using Vue.js communicating with API and hosted on google cloud",
                    "code":"https://github.com/khalidamairi3/vueTweeter.git",
                    "link" :"https://tweeeter.ml/#/",
                    "image": "https://cdn.dribbble.com/users/21059/screenshots/643154/tweet-count.png" 
                    },

                    { 
                    "title" : "Tweeter back-end" ,
                    "description" : "API impelementation for tweeter project that talks with SQL database and serve more than 20 functionalities",
                    "code":"https://github.com/khalidamairi3/tweeter_backend.git",
                    "link" : false,
                    "image": "https://i.stack.imgur.com/sHDyf.png"  
                    },

                    { 
                    "title" : "Okotoks-pizza" ,
                    "description" : "Restaurant responsive website project implemented with pure HTML and CSS (SASS)",
                    "code":"https://github.com/khalidamairi3/Okotoks.git",
                    "link" : "https://okotoks-pizza.ml/",
                    "image": "https://okopizza.ml/images/okotoks-pizza-logo.png"  
                    },
                    { 
                    "title" : "Blog Post App" ,
                    "description" : "CRUD blog post website that allows users to sign up and create an account. Login/logout functionality, create a post, delete a post, remove or approve comments, markdown and syntax highlighting to posts. Implemented using Django, Bootstrap, HTML, CSS, JavaScript and Python",
                    "code":"https://github.com/khalidamairi3/django_blog_app.git",
                    "link" : "https://blog-post-django-app.herokuapp.com/",
                    "image": "https://blog.tubikstudio.com/wp-content/uploads/2016/08/tubik-studio-logo-branding-design-1024x792.png"  
                    }

                    
                    
                    ]
            }
        },
        
    }
</script>

<style scoped>

#projects{   
    margin-top: 5vh;
    display: grid;
    grid-template-columns:repeat(auto-fit, minmax(350px, 1fr));
    justify-items: center;
    align-items: center;
    color: #fca311;
}


#projects-header{ 
    padding: 10px;
    grid-column: 1/-1;
    width: 40%;
    border-bottom: 2px solid;
    letter-spacing: 0.2rem;
    
}
</style>