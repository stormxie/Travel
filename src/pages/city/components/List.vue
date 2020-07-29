<template>
    <div class="list">
        <div class="area">
            <div class="title border-topbottom">当前城市</div>
            <div class="city-list">
                <div class="button-wrapper">
                    <div class="button">安宁</div>
                </div>
            </div>
        </div>
        <div class="area">
            <div class="title border-topbottom">当前城市</div>
            <div class="city-list">
                <div class="button-wrapper">
                    <div class="button">安宁</div>
                </div>
                <div class="button-wrapper">
                    <div class="button">安宁</div>
                </div>
                <div class="button-wrapper">
                    <div class="button">安宁</div>
                </div>
                <div class="button-wrapper">
                    <div class="button">安宁</div>
                </div>
                <div class="button-wrapper">
                    <div class="button">安宁</div>
                </div>
                <div class="button-wrapper">
                    <div class="button">安宁</div>
                </div>
            </div>
        </div>
        <div class="area">
            <div class="title border-topbottom">当前城市</div>
            <div class="city-list">
                <div class="button-wrapper">
                    <div class="button">安宁</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'List'
}
</script>

<style lang="stylus" scoped>
  @import '~style/varibles.styl'
  .border-topbottom
    &:before
      border-color #777
    &:after
      border-color #777
  .title
    padding-left .2rem
    font-size .26rem
    background #eee
    height .528rem
    line-height .528rem
    color $darkTextColor
  .city-list
    overflow hidden
    padding .1rem .6rem .1rem .1rem
    .button-wrapper
      float left
      width 33.3%
      .button
        text-align center
        background #fff
        margin .1rem
        border 1px solid #ccc
        border-radius .06rem
        height .5rem
        line-height .5rem
</style>
