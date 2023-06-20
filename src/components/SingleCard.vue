<template>
   <div class="card mb-3">
     <img class="card-img-top" :src="image" alt="Card image cap">
       <div class="card-body">
          <h5 class="card-title">
              {{ name }}
          </h5>
         <p class="card-text">
           {{ desc }}
         </p>
           <p class="card-text">
              <small class="text-muted">
                 Last updated 3 mins ago
              </small>
            </p>

      </div>
 </div>


</template>

<script>
export default {
    name: 'SingleCard',
    data(){
        return {

        }

    },
    props:{
        name : String,
        desc : String,
        image: String,
    }
}

</script>

<style lang="scss">

@import 'bootstrap/scss/bootstrap'

</style>