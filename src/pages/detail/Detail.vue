<template>
  <div>
    <detail-banner :sightName="sightName" :bannerImg="bannerImg" :galleryImgs="galleryImgs"></detail-banner>
  </div>
</template>

<script>
import axios from 'axios'
import DetailBanner from './components/Banner'

export default {
  name: 'Detail',
  components: {
    DetailBanner
  },
  data () {
    return {
      sightName: '',
      bannerImg: '',
      galleryImgs: []
    }
  },
  mounted () {
    this.getDetailInfo()
  },
  methods: {
    getDetailInfo () {
      axios.get('/api/detail.json')
        .then(this.getDetailInfoSucc)
    },
    getDetailInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.sightName = data.sightName
        this.bannerImg = data.bannerImg
        this.galleryImgs = data.galleryImgs
      }
    }
  }
}
</script>
