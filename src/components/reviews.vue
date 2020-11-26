<template>
    <div id="reviews">
        <h6 v-if="revs.length == 0"> There is no reviews to see</h6>
        <reviewItem v-for="rev in revs" :key="rev.id" :review = rev />
        <reviewForm />

    </div>
</template>

<script>
import reviewItem from "./review";
import reviewForm from "./reviewForm";
import axios from "axios";
    export default {
        name:"reviews-section",
        components: {
            reviewItem,
            reviewForm
                
        },
        mounted () {
            axios.request({
                url:"http://127.0.0.1:5000/api/reviews",
                method:"GET"
            }).then((response)=>{
                this.revs=response.data;
            }).catch(()=>{});
        },
        data() {
            return {
                revs:[]
            }
        },
    }
</script>

<style scoped>

#reviews{
    display: grid;
    justify-items: center;
    align-items: center;
    background-color: whitesmoke;
    width: 90%;
    grid-column: 1/-1;
}

@media only screen and ( min-width: 1000px) {

    #reviews {

        grid-template-columns: 1fr 1fr ;

    }




}


</style>