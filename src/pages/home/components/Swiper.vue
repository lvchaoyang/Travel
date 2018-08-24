<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1807/4f/37f83b87138a0c02.jpg_750x200_8e5df442.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/c5/8f384b861e4e9e02.jpg_750x200_29d574ba.jpg'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1807/66/e5a5cec881702f02.jpg_750x200_67bb5691.jpg'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/18/2dbce82b07a23402.jpg_750x200_14356b03.jpg'
      }]
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
