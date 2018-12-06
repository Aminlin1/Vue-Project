<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont head-back">&#xe624;</div>
    </router-link>
  </div>
</template>
<script>
export default {
  name: 'CityHeader'
}
</script>
<style scoped>
.header {
  position: relative;
  overflow: hidden;
  height: 0.86rem;
  line-height: 0.86rem;
  text-align: center;
  color: #fff;
  background: #00bce4;
  font-size: 0.35rem;
}
.head-back {
  width: 0.64rem;
  text-align: center;
  font-size: 0.4rem;
  position: absolute;
  top: 0;
  left: 0;
  color: #fff;
}
</style>
