<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" :src="bannerImg"/>
      <div class="banner-info">
        <div class="banner-title">
          {{sightName}}
          </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692;</span>
          {{this.bannerImgs.length}}
        </div>
      </div>
    </div>
    <fade-animation>
      <common-gallery :imgs="bannerImgs"
                     v-show="showGallery"
                     @close="handleGalleryClose">
      </common-gallery>
    </fade-animation>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
import FadeAnimation from 'common/fade/FadeAnimation'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallery,
    FadeAnimation
  },
  props: {
    sightName: String,
    bannerImg: String,
    bannerImgs: Array
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
