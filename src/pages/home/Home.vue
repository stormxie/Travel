<template>
<div>
    <home-header></home-header>
</div>
</template>

<script>
import HomeHeader from '@/pages/home/components/Header'
import HomeSwiper from '@/pages/home/components/Swiper'

export default {
  name: 'Home',
  data () {
    return {}
  },
  components: {
    HomeHeader,
    HomeSwiper
  }
}
</script>
