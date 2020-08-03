<template>
  <div class="container">
    <div class="banner" @click="handleBannerClick">
      <div class="backicon"></div>
      <div><img class="banner-img" :src="bannerImg"></div>
      <div class="banner-info">
        <div class="banner-title">
          {{sightName}}
        </div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe60b;</span> 2</div>
      </div>
    </div>
    <fade-animation>
      <gallery :galleryImgs="galleryImgs" class="gallery" v-show="inputGallery" @close="handleGalleryClick"></gallery>
    </fade-animation>
  </div>
</template>

<script>
import Gallery from 'common/gallery/Gallery'
import FadeAnimation from 'common/fade/FadeAnimation'
export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    galleryImgs: Array
  },
  data () {
    return {
      inputGallery: false
    }
  },
  components: {
    Gallery,
    FadeAnimation
  },
  methods: {
    handleBannerClick () {
      this.inputGallery = true
    },
    handleGalleryClick () {
      this.inputGallery = false
    }
  }
}
</script>

<style lang="stylus" scoped>
    .banner
      position relative
      width 100%
      height 0
      padding-bottom 55%
      .banner-img
        width 100%
      .banner-info
        position absolute
        display flex
        left 0
        right 0
        bottom 0
        color #fff
        background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
        .banner-title
          font-size .32rem
          height .6rem
          line-height .6rem
          flex 1
          padding 0 .2rem
        .banner-number
          height: .32rem
          line-height: .32rem
          margin-top: .14rem
          padding: 0 .4rem
          border-radius: .2rem
          background: rgba(0, 0, 0, .8)
          font-size: .24rem
          .banner-icon
            font-size: .24rem
</style>
