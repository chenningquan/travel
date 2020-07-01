<template>
<div>
  <home-header></home-header>
  <home-swiper></home-swiper>
  <home-icon-list></home-icon-list>
</div>
</template>

<script>
  import HomeHeader from './components/Header'
  import HomeSwiper from './components/Swiper'
  import HomeIconList from './components/IconList'
  export default {
    name: "Home",
    components: {
      HomeHeader,
      HomeSwiper,
      HomeIconList
    }
  }
</script>

<style scoped>

</style>
