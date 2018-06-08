<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/e5/59fad13a64807d02.jpg_750x200_713ae984.jpg'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/3b/ef86879aa50e3002.jpg_750x200_2a108508.jpg'
      }]
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
    padding-bottom 26.67%
    /* .swiper-pagination-bullet-active
      background-color red !important */ /* 不会起作用 */
    background-color #eee
    .swiper-img
      width 100%
</style>
