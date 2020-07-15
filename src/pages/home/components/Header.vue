<template>
    <div class="header">
        <div class="header-left"><span class="iconfont back-icon">&#xe624;</span></div>
        <div class="header-input">
          <span class="iconfont">&#xe632;</span>
          输入城市/景点/游玩主题
        </div>
        <div class="header-right">城市
          <span class="iconfont arrow-icon">&#xe64a;</span>
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
    display: flex
    background: $bgColor
    height: .86rem
    line-height .86rem
    color: #fff
    text-align center
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align center
        font-size .4rem
    .header-right
      width: 1.24rem
      float: right
      text-align center
      line-height .86rem
      .arrow-icon
        font-size .24rem
    .header-input
      flex: 1
      height .64rem
      line-height .64rem
      color #ccc
      text-align left
      background #fff
      border-radius .1rem
      padding-left .2rem
      margin-top .12rem
      margin-left .2rem
</style>
