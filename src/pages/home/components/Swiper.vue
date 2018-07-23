<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide>
        <img class="swiper-img" src="http://img1.qunarzz.com/piao/fusion/1807/4f/37f83b87138a0c02.jpg_750x200_8e5df442.jpg">
      </swiper-slide>
      <swiper-slide>
        <img class="swiper-img" src="http://img1.qunarzz.com/piao/fusion/1806/c5/8f384b861e4e9e02.jpg_750x200_29d574ba.jpg">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>

</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {}
    }
  }
}
</script>

<style scoped>
  .wrapper {
    overflow: hidden;
    width: 100%;
    height: 0;
    padding-bottom: 31.25%;
  }
  .swiper-img {
    width: 100%;
  }
</style>
