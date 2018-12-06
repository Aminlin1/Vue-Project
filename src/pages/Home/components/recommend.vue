<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title mixins">{{item.title}}</p>
          <p class="item-desc mixins">{{item.desc}}</p>
          <button class="item-button mixins">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeCommend',
  props: {
    list: Array
  }
}
</script>
<style scoped>
.title {
  margin-top: 0.2rem;
  line-height: 0.8rem;
  background: #eee;
  text-indent: 0.2rem;
}
.item {
  overflow: hidden;
  display: flex;
  height: 1.9rem;
}
.item-img {
  width: 1.7rem;
  height: 1.7rem;
  padding: 0.1rem;
}
.item-info {
  flex: 1;
  padding: 0.1rem;
  min-width: 0;
}
.item-title {
  line-height: 0.54rem;
  font-size: 0.32rem;
}
.item-desc {
  line-height: 0.4rem;
  color: #ccc;
}
.item-button {
  line-height: 0.44rem;
  margin-top: 0.16rem;
  background: #ff9300;
  padding: 0 0.2rem;
  border-radius: 0.06rem;
  color: #fff;
}
.mixins {
  overflow: hidden;
  /*如果页面文字过多  显示隐藏*/
  white-space: nowrap;
  text-overflow: ellipsis;
}
</style>
