<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <div class="item-img-weekend">
          <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title mixins">{{item.title}}</p>
          <p class="item-desc mixins">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
</script>
<style scoped>
.title {
  line-height: 0.8rem;
  background: #eee;
  text-indent: 0.2rem;
}
.item-img-weekend {
  position: relative;
  overflow: hidden;
  height: 0;
  padding: 18.55%;
}
.item-img {
  position: absolute;
  width: 375px;
  height: 139px;
  left: 1%;
  top: 1%;
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
  color: #616161;
}
.mixins {
  overflow: hidden;
  /*如果页面文字过多  显示隐藏*/
  white-space: nowrap;
  text-overflow: ellipsis;
}
</style>
