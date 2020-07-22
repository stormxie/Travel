<template>
<div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icon></home-icon>
</div>
</template>

<script>
import HomeHeader from '@/pages/home/components/Header'
import HomeSwiper from '@/pages/home/components/Swiper'
import HomeIcon from '@/pages/home/components/Icons'

export default {
  name: 'Home',
  data () {
    return {}
  },
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcon
  }
}
</script>
