<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-hot-sale></home-hot-sale>
    <home-like></home-like>
    <home-weekend></home-weekend>
  </div>
</template>
<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeHotSale from './components/HotSale'
import HomeLike from './components/Like'
import HomeWeekend from './components/Weekend'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHotSale,
    HomeLike,
    HomeWeekend
  }
}
</script>
<style>
</style>
