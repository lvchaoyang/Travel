<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1603/87/87146cf32fa8635e90.water.png_600x330_54030989.png"/>
      <div class="banner-info">
        <div class="banner-title">
          西湖(AAAAA景区)
          </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692;</span> 42
        </div>
      </div>
    </div>
    <CommonGallery :imgs="imgs"
                   v-show="showGallery"
                   @close="handleGalleryClose"></CommonGallery>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallery
  },
  data () {
    return {
      showGallery: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1412/f1/eac3ca9702975c292010cb728fbdbf6b.water.jpg_r_800x800_6fdb0f8d.jpg',
        'http://img1.qunarzz.com/sight/p0/1412/e8/2ec8d3c9acf5b5cb050760bb970b75bf.water.jpg_r_800x800_010971a8.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallery = true
    },
    handleGalleryClose () {
      this.showGallery = false
    }
  }
}
</script>

<style scoped>
  .banner {
    position: relative;
    overflow: hidden;
    height: 0;
    padding-bottom: 55%;
  }
  .banner-img {
    width: 100%;
  }
  .banner-info {
    display: flex;
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    line-height: .6rem;
    color: #fff;
    background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8));
  }
  .banner-title {
    flex: 1;
    font-size: .32rem;
    padding: 0 .2rem;
  }
  .banner-number {
    height: .32rem;
    line-height: .32rem;
    padding: 0 .4rem;
    margin-top: .14rem;
    border-radius: .2rem;
    font-size: .24rem;
    background: rgba(0, 0, 0, 0.8);
  }
  .banner-icon {
    font-size: .24rem;
  }
</style>
