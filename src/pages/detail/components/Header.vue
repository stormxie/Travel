<template>
    <div class="header">
        <router-link to="/" tag="div" class="header-abs" v-show="!showAbs">
            <span class="iconfont back-icon">&#xe624;</span>
        </router-link>
        <div class="header-fixed" :style="styleOpacity" v-show="showAbs">
            <router-link to="/">
            <div class="header-icon">
                <span class="iconfont back-icon">&#xe624;</span>
            </div>
            </router-link>
            <div class="header-content">
            城市选择
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: false,
      styleOpacity: {
        opacity: 0
      }
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll)
  },
  destroyed () {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll () {
      let top = document.documentElement.scrollTop || document.body.scrollTop || window.pageYOffset
      if (top > 60) {
        const opacity = top < 140 ? top / 140 : 1
        this.showAbs = true
        this.styleOpacity.opacity = opacity
      } else {
        this.showAbs = false
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~style/varibles.styl'
  .header
    color #fff
    text-align center
    .header-abs
      position absolute
      z-index 1
      margin .2rem 0 0 .2rem
      width .8rem
      height .8rem
      border-radius 50%
      background rgba(0, 0, 0, .7)
      .back-icon
        font-size .40rem
        line-height .8rem
    .header-fixed
      position fixed
      z-index 1
      top 0
      right 0
      left 0
      overflow hidden
      background $bgColor
      height .86rem
      line-height .86rem
      font-size .32rem
      .header-icon
        color #fff
        float left
        padding-left .14rem
        .back-icon
          font-size .4rem
      .header-content
        width 5rem
        position absolute
        left 0
        right 0
        margin auto
</style>
