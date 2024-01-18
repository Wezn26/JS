<template>
    <div>
        <h2>
            {{ foodName }}
            <img src="./../../public/img/img_quality.svg" 
            alt="img" v-show="isFavorite">
        </h2>
        <p>{{ foodDesc }}</p>
        <button v-on:click="toggleFavorite">Favorite</button>        
    </div>
</template>

<script>
    export default {
        props: ['foodName', 'foodDesc', 'isFavorite'],
        emits: ['toggle-favorite'],
        // data() {
        //     return {
        //         foodIsFavorite: this.isFavorite
        //     }
        // },
        methods: {
            toggleFavorite() {
                //this.foodIsFavorite = !this.foodIsFavorite
                this.$emit('toggle-Favorite', this.foodName);
            }
        },        
        // props: {
        //     foodName: {
        //         type: String,
        //         required: true
        //     },
        //     foodDesc: {
        //         type: String,
        //         required: false,
        //         default: 'This is the default description.',
        //         validator: function(value) {
        //             if (20 < value.length && value.length < 50) {
        //                 return true;
        //             } else {
        //                 return false;
        //             }
        //         }
        //     },
            // isFavorite: {
            //     type: Boolean,
            //     required: false,
            //     default: false
            // }
        }           
    
</script>

<style>
    img {
        height: 1.5em;
        float: right;
    }
</style>