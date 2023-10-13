
<script>
import { store } from '../data/store';
import MonsterCard from './partials/MonsterCard.vue';

export default {
    name: 'CardsContainer',
    components: {
        MonsterCard
    },
    data(){
        return{
            store
        }
    },
    mounted(){
        console.log(store.cardList);
    }
}
</script>


<template>
    <main>
        <div class="select">
            <select name="Archetype" id="" placeholder="Select"> </select>
        </div>
    <body>
        
        <div class="content">
            <div class="container-fluid">
                <div class="row">
                    <div class="info"></div>
                      <MonsterCard
                        v-for="card in store.cardList"
                        :key="card.id" 
                        :imgObj="card.card_images[0].image_url_small"
                        :titileObj="card.name"
                        :typeObj="card.archetype"
                      />                    
                </div>
            </div>
       
        </div>

    </body>

    </main>
  
</template>



<style lang="scss" scoped>

@use '../scss/partials/vars' as *;

  main{
    background-color: $primary-color;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }
  body{
    width: 80%;
  }

  .select{
    height: 80px;
    display: flex;
    width: 80%;
    align-items: center;
    select{
        height: 30px;
        width: 100px;
        z-index: 1;
    }
  }
  .row{
    margin: 20px;
  }
  .info{
    width: 100%;
    height: 50px;
    background-color: #212529;
    margin-right: calc(var(--bs-gutter-x) * 0.5);
    margin-left: calc(var(--bs-gutter-x) * 0.5);
    flex-shrink: 1;
    margin-top: 20px;
  }
</style>