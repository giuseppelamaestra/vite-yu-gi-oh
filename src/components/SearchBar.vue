<script>

export default{
    name: 'SearchBar',
    components: {

    },
    props:{
        archetypeList: Array
    }
}

</script>

<template>
   <div class="my-searchbar">
        <select name="card-archetype">
            <option v-for="archetype in archetypeList" :value="archetype.archetype_name">

                {{ archetype.archetype_name }}
            </option>
        </select>
    </div>
    
</template>

<style lang="scss" scoped>
div.my-searchbar { 

    


}
</style>