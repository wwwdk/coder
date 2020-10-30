<template>
  <div>
    <div class="header">
      <div class="header-left">
        <div class="iconfont">
          &#xe684;
        </div>
      </div>
      <div class="header-input">景点</div>
      <div class="header-right">城市</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  data () {
    return {
      msg: 'HomeHeader'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
  .header
    display: flex
    line-height: .86rem
    background: #00bcd4
    color: #ffffff
    .header-left
      width: .64rem
      color: #ccc
    .header-input
      flex: 1
      margin-top: .12rem
      margin-left: .2rem
      height: .62rem
      line-height: .62rem
      border-radius: .1rem
      background: #ffffff
      color: #cccccc
    .header-right
      width: 1.44rem
      float: right
      text-align: center
</style>
