<template>
  <div class="home">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recommend></home-recommend>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeHeader from './components/Header.vue'
import HomeSwiper from './components/Swiper.vue'
import HomeIcons from './components/Icons.vue'
import HomeRecommend from './components/Recommend.vue'

export default {
  name: 'home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend
  }
}
</script>
