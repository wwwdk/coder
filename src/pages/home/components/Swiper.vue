<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
        <!-- slides -->
        <!-- <div v-for = "item in list">{{item}}</div> -->
        <swiper-slide v-for="item in swiperList" :key="item.id">
          <img class="swiper-img" :src="item.imgUrl" alt="">
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
        <!-- <div class="swiper-button-prev" slot="button-prev"></div>
        <div class="swiper-button-next" slot="button-next"></div>
        <div class="swiper-scrollbar"   slot="scrollbar"></div> -->
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
      swiperList: [
        {
          id: '001',
          imgUrl: '//imgs.qunarzz.com/vc/e3/a1/71/f498dfd3bed948d623c9093252.jpg_92.jpg'
        },
        {
          id: '002',
          imgUrl: '//imgs.qunarzz.com/vs_ceph_vcimg/c0a60fa20379efa4f02ce527a680dc1b.jpeg'
        },
        {
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1712/91/a275569091681d02.jpg_640x200_0519ccb9.jpg'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active //修改子组件样式
  background #fff
.wrapper
  width 100%
  height 0
  padding-bottom 30%
  overflow hidden
.swiper-img
  width 100%
</style>
