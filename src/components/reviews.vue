<template>
    <div id="reviews">
        <h5 style="grid-column: 1/-1" v-if="revs.length == 0"> There is no reviews to see</h5>
        <reviewItem v-for="rev in revs" :key="rev.id" :review = rev />
        <reviewForm @addReview="addrev" />

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
                url:"https://khaledamayri.com/api/reviews",
                method:"GET"
            }).then((response)=>{
                this.revs=response.data.reverse();
            }).catch(()=>{});

        },
        data() {
            return {
                revs:[]
            }
        },
        methods: {
            addrev:function(data) {
                console.log(data);
                this.revs.unshift(data);
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