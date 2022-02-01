<template>
  <div id="app">
    <Header/>
    <main-container :personaggi="personaggi"/>

    
  </div>
</template>

<script>

import MainContainer from './components/MainContainer.vue'
import Header from './components/Header.vue'
import axios from 'axios'


export default {
  name: 'App',
  components: {
  MainContainer,
  Header,
},

data() {
  return {
    personaggi:[]
  }
},


mounted() {
  axios.get('https://api.sampleapis.com/rickandmorty/characters').then((response)=> {
    this.personaggi=response.data;
  })
 }
}
</script>

<style lang="scss">
@import './style/main.scss';
</style>
