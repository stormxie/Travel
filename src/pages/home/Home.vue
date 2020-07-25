<template>
<div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icon></home-icon>
    <home-recommend></home-recommend>
</div>
</template>

<script>
import HomeHeader from '@/pages/home/components/Header'
import HomeSwiper from '@/pages/home/components/Swiper'
import HomeIcon from '@/pages/home/components/Icons'
import HomeRecommend from '@/pages/home/components/Recommend'

export default {
  name: 'Home',
  data () {
    return {}
  },
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcon,
    HomeRecommend
  }
}
</script>
