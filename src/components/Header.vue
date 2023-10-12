<script>
export default {
    name: 'Header',
    props: {
        titleStr: String
    }
}
</script>


<template>
  <div class="logo">
    <!-- <img src="../../public/Yugioh_anime_logo.webp" alt="" -->
    <h1>{{ titleStr }}</h1>
  </div>
</template>



<style>

</style>