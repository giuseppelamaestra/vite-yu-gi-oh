<template>

    <main>
       <CardsList/>
    </main>
  
</template>
<script>
 import CardsList from './CardsList.vue'
 

 export default {
    name: 'AppMain',
    data() {
        return {
 
           } 
     }, 

     components: {
        CardsList
     },

     

        
 }
</script>
<style lang="scss">
@import 'bootstrap/scss/bootstrap'
</style>