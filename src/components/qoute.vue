<template>
    <div id="qoute">
        <h1 id="qoute-header"> Get a Qoute </h1>
        <label for="name"> Name: </label>
        <input type="text" name="name">
        <label for="email"> Email:</label>
        <input name="email" type="text" v-model="email">
        <label for="description"> Description: </label>
        <textarea name="description" id="text" v-model="text" ></textarea>

        <button> Submit </button>


    </div>
</template>

<script>
    export default {
        name:"qoute-section",
        data() {
            return {
                name:"",
                email: "",
                text:""

            }
        },
    }

</script>

<style scoped>
#qoute{
    width: 100%;
    display: grid;
    align-items: center;
    justify-items: center;
    border :10px solid #fca311;
    background-color:#14213d ;
    color:white ;
    grid-template-columns: 2fr 4fr;
    row-gap: 5vh;
    padding-bottom: 5vh;
}

#qoute-header{
    grid-column: 1/-1;
    border-bottom: 2px solid;
    padding-bottom: 10px;
}

input{
    width: 80%;
    border: 2px solid #fca311;
    height: 5vh;
    
}
button{
    font-size: 1.5em;
    grid-column: 1/-1;
    border: none;
    color: white;
    background: #fca311;
    border-radius: 15px;
    padding: 15px;
}

label{
    font-size: 1.5em;
}

textarea{
    width: 80%;
    height: 30vh;
    border: 2px solid #fca311;
}
</style>