<template>
  <div class="icons">
    <div class="icon">
      <div class="icon-img">
        <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png" alt="">
      </div>
      <p>热门景点</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons'
}
</script>

<style lang="stylus" scoped>
  .icons
    width 100%
    overflow hidden
    height 0
    padding-bottom 50%
    background-color green
    .icon
      height 0
      position relative
      overflow hidden
      float left
      width 25%
      padding-bottom 25%
      background-color red
      .icon-img
        position absolute
        top 0
        right 0
        left 0
        bottom 0.44rem
        box-sizing border-box
        padding 0.1rem
        background-color blue
        .icon-img-content
          display block
          margin 0 auto
          height 100%
</style>
