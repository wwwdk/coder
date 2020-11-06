<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item in page" :key="item.id">
          <img class="icon-img" :src="item.iconUrl" alt="">
          <span class="icon-description">{{item.iconDescription}}</span>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      iconList: [
        {
          id: '001',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png',
          iconDescription: '景点门票'
        },
        {
          id: '002',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1711/df/86cbcfc533330d02.png',
          iconDescription: '滑雪季'
        },
        {
          id: '003',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1710/a6/83f636bd75ae6302.png',
          iconDescription: '泡温泉'
        },
        {
          id: '004',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1611/35/2640cab202c41b02.png',
          iconDescription: '动植园'
        },
        {
          id: '005',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1611/d0/e09575e66f4aa402.png',
          iconDescription: '游乐园'
        },
        {
          id: '006',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1611/59/569d3c096e542502.png',
          iconDescription: '必游榜单'
        },
        {
          id: '007',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1611/17/4bd370f3eb1acd02.png',
          iconDescription: '演出'
        },
        {
          id: '008',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1611/7f/b1ea3c8c7fb6db02.png',
          iconDescription: '城市观光'
        },
        {
          id: '009',
          iconUrl: 'http://img1.qunarzz.com/piao/fusion/1611/a9/ffc620dbda9b9c02.png',
          iconDescription: '一日游'
        }
      ]
    }
  },
  computed: {
    pages () {
      var pages = []
      this.iconList.forEach((item, index) => {
        var page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
.icons
  width 100%
  height 0
  padding-bottom 50%
  overflow hidden
  .icon
    position relative
    overflow hidden
    float left
    width 25%
    height 0
    background #fff
    padding-bottom 25%
    .icon-img
      position absolute
      margin 0 auto
      height 100%
      top 0
      left 0
      right 0
      padding .35rem
      box-sizing border-box
    .icon-description
      position absolute
      left 0
      right 0
      bottom 0
      text-align center
      overflow hidden
      white-space nowrap
      text-overflow ellipsis
</style>
