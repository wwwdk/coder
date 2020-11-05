<template>
  <div>
    <home-header></home-header>
    <home-swipper></home-swipper>
    <div class="home">
      <h1>Home</h1>
    </div>
    <router-link to="list">列表页</router-link>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwipper from './components/Swipper'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwipper
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home{
  text-align: center;
}
</style>
