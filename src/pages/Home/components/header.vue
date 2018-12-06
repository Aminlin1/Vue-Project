<template>
  <div class="header bgcolor">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span> 输入城市/景点/游玩主题
    </div>
    <router-link to='/city'>
      <div class="header-right">
        北京
        <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>
<style scoped>
.header {
  display: flex;
  line-height: 0.86rem;
  color: #fff;
}
.header-left {
  width: 0.64rem;
  float: left;
}
.header-input {
  height: 0.64rem;
  line-height: 0.64rem;
  flex: 1;
  margin-top: 0.12rem;
  margin-left: 0.2rem;
  background: #fff;
  border-radius: 0.1rem;
  color: #ccc;
  padding-left: 0.2rem;
}
.header-right {
  width: 1.24rem;
  float: right;
  text-align: center;
  color: #fff;
}
.back-icon {
  text-align: center;
  font-size: 0.4rem;
}
.arrow-icon {
  font-size: 0.2rem;
  margin-left: -0.04rem;
}
.bgcolor {
  background: #00bce4;
}
</style>
