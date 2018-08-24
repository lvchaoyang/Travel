<template>
  <div class="#home">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
  </div>
</template>
<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
export default {
  name: 'home',
  components: {HomeIcons, HomeSwiper, HomeHeader}
}
</script>

<style scoped>

</style>
