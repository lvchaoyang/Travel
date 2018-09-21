<template>
  <div>
    <detail-banner
      :sightName="sightName"
      :bannerImg="bannerImg"
      :bannerImgs="galleryImg"
    ></detail-banner>
    <detail-header></detail-header>
    <div class="content">
      <detail-list :list="list"></detail-list>
    </div>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
import axios from 'axios'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      id: '',
      sightName: '',
      bannerImg: '',
      galleryImg: [],
      list: []
    }
  },
  methods: {
    getDetailInfo () {
      axios.get('/api/detail.json', {
        params: {
          id: this.$route.params.id
        }
      }).then(this.handleGetDataSucc)
    },
    handleGetDataSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.sightName = data.sightName
        this.bannerImg = data.bannerImg
        this.galleryImg = data.galleryImg
        this.list = data.categoryList
      }
    }
  },
  mounted () {
    this.id = this.$route.params.id
    this.getDetailInfo()
  },
  activated () {
    if (this.id !== this.$route.params.id) {
      this.id = this.$route.params.id
    }
    this.getDetailInfo()
  }
}
</script>

<style scoped>
</style>
