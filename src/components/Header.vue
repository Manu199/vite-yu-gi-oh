<script>
export default {
    name: 'Header',
    props: {
        titleStr: String
    }
}
</script>


<template>
    <header>
        <div class="logo">
            <img  src="../../public/Yugioh_anime_logo.webp" alt="">
        </div>
        <h1>{{ titleStr }}</h1>
    </header>
  
</template>



<style lang="scss" scoped>

header {
    display: flex;
    align-items: center;
    height: 50px;
 h1{
    font-size: 2rem;
    margin-left: 10px;
    }
}
.logo {

    img{
        width: 50px;
        margin-bottom: 5px;
        margin-left: 20px;
    }
}


</style>