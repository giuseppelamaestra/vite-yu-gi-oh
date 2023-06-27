<template>

    <main>

      <SearchBar
        :archetypeList="archetypeList"/>
       <CardsList/>

    </main>
  
</template>
<script>
 import CardsList from './CardsList.vue'
 import SearchBar from './SearchBar.vue'
 import axios from 'axios';
 import { store } from '../store.js';

 

 export default {
    name: 'AppMain',
    components:{
    CardsList,
    SearchBar,

    
    },
    data(){
        return{
            archetypeList:[],
        }
    },
    created(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
            .then(function (response) {
                console.log(response.data.data);
                store.listApi = response.data.data;
            })
            .catch(function (error) {
                console.log(error);
            }),
        axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            .then(response => {
                console.log(response.data);
                this.archetypeList = [...response.data];
            })
            .catch(function (error) {
                console.log(error);
            })
    }
        
}
</script>
<style lang="scss">
@import 'bootstrap/scss/bootstrap'
</style>