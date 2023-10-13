<script>

export default {
 name: 'MonsterCard',
 props:{

  imgObj: String,
  titleObj: String,
  typeObj: String,
  // cardData: Object,
  
 },
//  computed: {
//     cardImageUrl() {
//       return `https://images.ygoprodeck.com/images/cards/${this.cardData.id}.jpg`;
//     },
//   },
}
</script>

<template>
  <div class="ms-col">
    <div class="ms-card">
       <img src="imgObj" alt="">
       <div>
        <p>{{ titleObj }}</p>
        <span>{{ typeObj }}</span>
       </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>

@use '../../scss/partials/vars' as *;

.ms-col {
  width: 20%;
}
.ms-card{
  background-color: $primary-color;
  div{
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    p{
      padding-top: 10px;
      color: white;
    }
  }
}
    img{
        width: 100%;
    }
</style>