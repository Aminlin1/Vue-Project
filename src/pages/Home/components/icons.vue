<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-image">
            <img class="icon-image-2" :src="item.imgUrl">
          </div>
          <p class="icons-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeIcons',
  props: {
    list: Array
  },
  computed: {
    pages () {
      const pages = []
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8)
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
<style scoped>
.icons {
  margin-top: 0.1rem;
}
.icons >>> .swiper-container {
  height: 0;
  padding-bottom: 50%;
}
.icon {
  position: relative;
  overflow: hidden;
  float: left;
  width: 25%;
  padding-bottom: 25%;
  height: 0;
}
.icon-image {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0.44rem;
  right: 0;
}
.icon-image-2 {
  height: 100%;
  display: block;
  margin: 0 auto;
  box-sizing: border-box;
  padding: 0.1rem;
}
.icons-desc {
  position: absolute;
  left: 0px;
  bottom: 0;
  right: 0;
  text-align: center;
  height: 0.44rem;
  line-height: 0.44rem;
  color: #333;
  overflow: hidden;
  /*如果页面文字过多  显示隐藏*/
  white-space: nowrap;
  text-overflow: ellipsis;
}
</style>
