<template>
  <div id="app">
    <Header />
    <OfferSection />
    <CardSection />

    <CardQuestion />


  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import OfferSection from './components/OfferSection.vue'
import CardSection from './components/CardSection.vue'
import CardQuestion from './components/CardQuestion.vue'

</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap');
@import './assets/css/main.css';

</style>
