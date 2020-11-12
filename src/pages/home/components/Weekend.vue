<template>
  <div>
    <div class="title">周末去哪儿</div>
    <div class="item" v-for="weekend in weekendList" :key="weekend.id">
      <div class="item-img-wrapper">
        <img class="item-img" :src="weekend.itemUrl" alt="">
      </div>
      <div class="item-info">
        <div class="item-title">{{weekend.itemTitle}}</div>
        <div class="item-desc">{{weekend.itemDesc}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      msg: 'HomeWeekend',
      weekendList: [{
        id: '0001',
        itemUrl: 'http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg',
        itemTitle: '北京温泉排行榜',
        itemDesc: '细数北京温泉，温暖你的冬天'
      }, {
        id: '0002',
        itemUrl: 'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg',
        itemTitle: '北京必游TOP10',
        itemDesc: '来北京必去的景点非这些地方莫属'
      }, {
        id: '0003',
        itemUrl: 'http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg',
        itemTitle: '寻找北京的皇城范儿',
        itemDesc: '数百年的宫廷庙宇，至今依旧威严霸气'
      }, {
        id: '0004',
        itemUrl: 'http://img1.qunarzz.com/sight/source/1505/ce/bc89bc2f0e33ea.jpg_r_640x214_3e408453.jpg',
        itemTitle: '学生最爱的博物馆',
        itemDesc: '周末干嘛？北京很多博物馆已经免费开放啦'
      }, {
        id: '0005',
        itemUrl: 'http://img1.qunarzz.com/sight/source/1505/b2/fde1bfcd057a52.jpg_r_640x214_bbf3fa44.jpg',
        itemTitle: '儿童剧场，孩子的乐园',
        itemDesc: '带宝贝观看演出，近距离体验艺术的无穷魅力'
      }]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
@import '~@/assets/styles/mixins.styl';
.title
  line-height .8rem
  background #eee
  text-indent .2rem
.item-img-wrapper
  height 0
  padding-bottom 37%
  .item-img
    width 100%
.item-info
  padding .1rem
  min-width 0
  .item-title
    line-height .5rem
    font-size .3rem
  .item-desc
    line-height .4rem
    color #aaa
    ellipsis()
</style>
