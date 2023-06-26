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
    data(){
        return {
            CardsList : [],
            store
        }

    },
    components:{
        SingleCard,
    },

    created(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')

        .then((response) => {
            this.CardsList = response.data.data;

        })
      

        
    }
}
</script>
<style lang="scss">

</style>