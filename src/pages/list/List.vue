<template>
  <div>
    <div class="list">
      <h1>List</h1>
    </div>
    <router-link to="home">返回主页</router-link>
  </div>
</template>

<script>
export default {
  name: 'List'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.list{
  text-align: center;
}
</style>
