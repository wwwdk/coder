<template>
  <div>
    <div class="header">
      <div class="header-left">
        <span class="iconfont back-icon">
          &#xe696;
        </span>
      </div>
      <div class="header-input">
        <span class="iconfont">
          &#xe613;
        </span>
        输入城市/景点/游玩主题
      </div>
      <div class="header-right">
        城市
        <span class="iconfont arrow-icon">
          &#xe60a;
        </span>
      </div>
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
      text-align: center
      .back-icon
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      margin-top: .15rem
      margin-left: .1rem
      height: .62rem
      line-height: .62rem
      border-radius: .1rem
      background: #ffffff
      color: #cccccc
    .header-right
      width: 1.44rem
      float: right
      text-align: center
      line-height .86rem
      .arrow-icon
        font-size .24rem
</style>
