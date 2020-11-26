<template>
    <div id="review"  data-aos="flip-down" data-aos-duration ="1000">
        <h3> {{ review.name }} </h3>
        <span> {{ review.date }}</span>
        <p> {{ review.message }}</p>
        <ul  class="rating">
    <li   class="rating-item" v-bind:class="{ active : 1==review.rate }" data-rate="1"></li>
    <li  class="rating-item" v-bind:class="{ active : 2==review.rate }" data-rate="2"></li>
    <li  class="rating-item" v-bind:class="{ active : 3==review.rate }" data-rate="3"></li>
    <li  class="rating-item" v-bind:class="{ active : 4==review.rate }" data-rate="4"></li>
    <li  class="rating-item" v-bind:class="{ active : 5==review.rate }" data-rate="5"></li>
    </ul>

    </div>
</template>

<script>
    export default {
        name:"review-section",
        props: {
            review: {
                type: Object,
                required:true
            },
        },
    }
</script>

<style scoped>
#review{
    
    width: 80%;
    display: grid;
    align-items: center;
    justify-items: start;
    margin-left: 10%;
    text-align: justify;
}

.rating {
justify-self: center;
display: flex;
padding: 0;
margin: 0;
}

.rating li {
list-style-type: none
}

.rating-item {
border: 1px solid #fff;
font-size:2em;
color: #fca311;
}

/* initial: make all stars full */
.rating-item::before {
content: "\2605";
}

/* make until the clicked star (the rest) empty */
.rating-item.active ~ .rating-item::before {
content: "\2606";
} 

/* on hover make all full */
/* .rating:hover .rating-item::before {
content: "\2605";
}  */

/* make until the hovered (the rest) empty */
/* .rating-item:hover ~ .rating-item::before {
content: "\2606";
}  */

</style>