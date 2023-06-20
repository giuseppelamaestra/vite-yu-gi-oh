<template>
  
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
            console.log(response.data.results);

        })
        .catch(function (error){
            console.log(error)
    })

        
    }
}
</script>
<style lang="scss">

</style>