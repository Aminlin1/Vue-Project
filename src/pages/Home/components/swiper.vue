<template>
  <div class="war">
    <swiper :options="swiperOption" v-if="list.length">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" key="item.id" />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: '2500'
      }
    }
  }
}
</script>
<style scoped>
.war >>> .swiper-pagination-bullet-active {
  background: #fff;
}
.swiper-img {
  width: 100%;
}
.war {
  overflow: hidden;
  width: 100%;
  height: 0px;
  padding-bottom: 27%;
}
</style>
