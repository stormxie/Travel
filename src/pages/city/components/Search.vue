<template>
    <div class="search">
        <input class="search-input" type="text" placeholder="输入城市名称或拼音">
    </div>
</template>

<script>
export default {
  name: 'Search'
}
</script>

<style lang="stylus" scoped>
  @import '~style/varibles.styl'
  .search
    background $bgColor
    height .62rem
    padding 0 .1rem .14rem .1rem
    .search-input
      text-align center
      border-radius .06rem
      height .62rem
      width 100%
</style>
