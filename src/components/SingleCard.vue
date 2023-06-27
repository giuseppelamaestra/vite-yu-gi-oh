<template>
   <div class="card mb-3">
     <img class="card-img-top" :src="image" alt="Card image cap">
       <div class="card-body">
          <h5 class="card-title">
              {{ name }}
          </h5>
         <p class="card-text">
           {{ type }}
         </p>
         <div class="my-cards-element">
        <img :src="SingleCard.card_images[0].image_url" :alt="SingleCard.name + 'Image'">
        <h3>{{ SingleCard.name }}</h3>
        <span>{{ SingleCard.archetype }}</span>
    </div>
            

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
        singleCard: Object,
    }
}

</script>

<style lang="scss">



.my-cards-element{
  width: calc(100% / 5);
}

</style>