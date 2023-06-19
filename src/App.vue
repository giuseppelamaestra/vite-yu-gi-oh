<script setup>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import CardsList from './components/CardsList.vue'
import SingleCard from './components/SingleCard.vue'
</script>

<template>
  <AppHeader/>
  <AppMain/>
  <CardsList/>
  <SingleCard/>
</template>

<style lang="scss">
@import 'bootstrap/scss/bootstrap';
@import './styles/general.scss';

</style>
