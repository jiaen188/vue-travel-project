<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
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
        loop: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  /* 让样式穿透，因为我们为swiper-pagination-bullet-active添加的样式，是组件内的样式，并且是scoped,所以正常写法不起作用 */
  .wrapper >>> .swiper-pagination-bullet-active
    background-color #fff !important
  .wrapper
    overflow hidden
    width 100%
    height 0 /* 不能设置height是31.25%，因为是相对父级的百分比 */
    padding-bottom 31.25%
    /* .swiper-pagination-bullet-active
      background-color red !important */ /* 不会起作用 */
    background-color #eee
    .swiper-img
      width 100%
</style>
