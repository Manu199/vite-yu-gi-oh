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
        
        <div class="container">
            <div class="row">
               <MonsterCard />
               <MonsterCard />
               <MonsterCard />
               <MonsterCard />
               <MonsterCard />
            </div>
        </div>
        
    </main>
  
</template>



<style lang="scss" scoped>

</style>