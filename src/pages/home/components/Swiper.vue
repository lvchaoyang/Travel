<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="list.length">
      <!-- slides -->
      <swiper-slide v-for="item in list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  }
}
</script>

<style scoped>
  .wrapper {
    overflow: hidden;
    width: 100%;
    height: 0;
    padding-bottom: 26.7%;
  }

  .swiper-img {
    width: 100%;
  }

  .wrapper >>> .swiper-pagination-bullet-active {
    background: #ffffff;
  }
</style>
