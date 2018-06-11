<template>
  <div>
    <div class="title">
      热销推荐
    </div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <img :src="item.imgUrl" class="item-img">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top .2rem
    line-height 0.8rem
    background-color #eee
    text-indent .2rem
  .item
    overflow hidden
    display flex
    height 1.9rem
    .item-img
      width 1.7rem
      height 1.7rem
      padding 0.1rem
    .item-info
      flex 1
      padding 0.1rem
      min-width 0  /* 省略号样式不起作用，加上这句 */
      .item-title
        line-height 0.54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height 0.4rem
        color #ccc
        ellipsis()
      .item-button
        line-height 0.44rem
        margin-top 0.16rem
        background-color #ff9300
        padding 0 .2rem
        border-radius 0.06rem
        color #fff
</style>
