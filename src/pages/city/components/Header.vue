<template>
    <div class="header">
        <router-link to="/">
            <div class="header-icon">
                <span class="iconfont back-icon">&#xe624;</span>
            </div>
        </router-link>
        <div class="header-content">
            城市选择
        </div>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  data () {
    return {}
  }
}
</script>

<style lang="stylus" scoped>
  @import '~style/varibles.styl'
  .header
    background $bgColor
    position relative
    height .86rem
    line-height .86rem
    text-align center
    font-size .32rem
    color #fff
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
