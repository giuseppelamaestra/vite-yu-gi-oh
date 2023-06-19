<template>

    <main>
        <div class="container">
           <div class="container-card">
            <SingleCard/>
           </div>
        </div>
    </main>
  
</template>
<script>
 import SingleCard from './SingleCard.vue'
 import axios from 'axios'

 export default {
    name: 'AppMain',
    data() {
        return {
 
           } 
     }, 

     components: {
        SingleCard
     },

     created () {
        const axios = require('axios');

      // Make a request for a user with a given ID
       axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
       .then(function (response) {
       // handle success
       console.log(response);
       })
      .catch(function (error) {
        // handle error
       console.log(error);
       })
       .finally(function () {
         // always executed
         });

     }


        
 }
</script>
<style lang="scss">
@import 'bootstrap/scss/bootstrap'
</style>