<template>
    <div class="flex flex-wrap">
    <SingleCard v-for="card in CardsList" :cardName="card.name" :cardImg="card.card_images[0].image_url" :cardArchetype="card.archetype"/>
    </div>
</template>
<script>
import SingleCard from './SingleCard.vue';
import axios from 'axios';
import { store } from '../store.js';

export default {
    name: 'CardsList',
    components: {
        SingleCard,
    },
    data(){
        return{
            apiUrl:'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0', 
            cardsList : [],
        }
    },
   
    
    created(){
        axios.get(this.apiUrl)
        .then( (response) => {
           
            console.log(response.data.data[0].card_images);
            this.cardsList = response.data.data;
        })
        .catch(function (error) {
            
            console.log(error);
        });
    },
    data () {
        return {
            store
        }
    },
}
              
</script>
<style lang="scss">

</style>