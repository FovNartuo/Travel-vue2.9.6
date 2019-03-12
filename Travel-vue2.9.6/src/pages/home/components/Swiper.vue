<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>

      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>
<style lang="stylus" scoped>
  /*样式穿透*/
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff !important
  .wrapper
    //图片宽高比例自适应方案
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 26.67%  //原始图片高宽之比是26.67%
    background: #eee
    .swiper-img
      width: 100%
</style>
