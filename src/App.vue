<script>

import axios from 'axios';
import Header from './components/Header.vue'
import { store } from './data/store'

export default {
  name: 'App',
  components: {
    Header
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
  <Header titleStr="Yu Gi Oh"/>

</template>


<style lang="scss" >

@use './scss/main.scss';



</style>