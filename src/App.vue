<script>

import axios from 'axios';
import Header from './components/Header.vue'
import { store } from './data/store'
import CardsContainer from './components/CardsContainer.vue';

export default {
  name: 'App',
  components: {
    Header,
    CardsContainer
  },
  data(){
    return{
      store
    }
  },
  methods:{
    getApi(){
      axios.get(store.apiUrl)
      .then( res => {
        store.cardList = res.data.data
        console.log(res.data);
      })
      .catch(err => {
        console.log(errorrrrr);
      })
    }
  },
  mounted(){
    this.getApi();
  }
}
</script>


<template>
  <Header titleStr="Yu-Gi-Oh Api"/>
  <CardsContainer />
</template>


<style lang="scss" >

@use './scss/main.scss';



</style>