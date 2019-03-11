<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" >
        <div class="item-info">
          <p class="item-title" v-text="item.title"></p>
          <p class="item-desc" v-text="item.desc"></p>
          <button class="item-button">查看详情</button>
        </div>

      </li>
    </ul>
  </div>

</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1511/ea/eaf1bdc38aed9e6690.img.jpg_200x200_3032bf56.jpg',
        title: '银杏湖乐园',
        desc: '南京游玩首站，银杏湖乐园期待您的到来'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/f4/f455d92ba582f608.water.jpg_200x200_375e5775.jpg',
        title: '南京汤山颐尚温泉',
        desc: '南京游玩第二站，汤山颐尚温泉期待您的到来'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1502/e1/e1834f8d1ed57517.water.jpg_200x200_a9e76b67.jpg',
        title: '南京梅花节',
        desc: '三月游南京，不可错过的梅花节'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@/assets/styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.8rem
      height: 1.8rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width 0
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .2rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color:#fff
</style>
