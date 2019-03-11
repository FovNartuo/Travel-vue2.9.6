<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>

      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20192/6b46758091cd0220be1226236596b552.jpg_750x200_165648c8.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/2f5f3ea4698c9b7898db7562d89b91ed.jpg_750x200_bd3b4ce9.jpg'
      }]
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
