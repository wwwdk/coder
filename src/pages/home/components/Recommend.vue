<template>
  <div>
    <div class="title">热销推荐</div>
    <div class="item" v-for="recommend in recommendList" :key="recommend.id">
      <img class="item-img" :src="recommend.itemUrl" alt="">
      <div class="item-info">
        <div class="item-title">{{recommend.itemTitle}}</div>
        <div class="item-desc">{{recommend.itemDesc}}</div>
        <button class="item-button">查看详情</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      msg: 'HomeRecommend',
      recommendList: [
        {
          id: '0001',
          itemUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_140x140_80f63803.jpg',
          itemTitle: '故宫',
          itemDesc: '东方宫殿建筑代表，世界宫殿建筑典范'
        }, {
          id: '0002',
          itemUrl: 'http://img1.qunarzz.com/sight/p0/1511/d2/d2aec2dfc5aa771290.water.jpg_140x140_abb362a7.jpg',
          itemTitle: '南山滑雪场',
          itemDesc: '北京专业级滑雪圣地'
        }, {
          id: '0003',
          itemUrl: 'http://img1.qunarzz.com/sight/p0/1501/f4/f467729126949c3a.water.jpg_140x140_ef235b1c.jpg',
          itemTitle: '天安门广场',
          itemDesc: '我爱北京天安门，天安门上太阳升'
        }, {
          id: '0004',
          itemUrl: 'http://img1.qunarzz.com/sight/p0/1501/40/40b2b6c951b28fdd.water.jpg_140x140_1c863e5c.jpg',
          itemTitle: '水立方',
          itemDesc: '中国的荣耀，阳光下的晶莹水滴'
        }, {
          id: '0005',
          itemUrl: 'http://img1.qunarzz.com/sight/p0/201308/23/b283071686e64dfec8d65eac.jpg_140x140_8c5a7c49.jpg',
          itemTitle: '温都水城养生馆',
          itemDesc: '各种亚热带植物掩映其间仿佛置身热带雨林'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
.title
  line-height .8rem
  background #eee
  text-indent .2rem
.item
  display flex
  overflow hidden
  height 1.9rem
  .item-img
    width 1.7rem
    height 1.7rem
    padding .1rem
  .item-info
    flex 1
    padding .1rem
    min-width 0
    .item-title
      line-height .5rem
      font-size .3rem
    .item-desc
      line-height .4rem
      color #aaa
    .item-button
      line-height .44rem
      background #ff9311
      border-radius .08rem
      padding 0 .2rem
      color #fff
      margin-top 0.1rem
</style>
