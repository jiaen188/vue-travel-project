<template>
  <div class="icons">
    <swiper v-if="pages.length" :options="swiperOption">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div
          class="icon"
          v-for="item of page"
          :key="item.id"
        >
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
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
  data () {
    return {
      swiperOption: {
        loop: true,
        // effect: 'fade',
        autoplay: {
          delay: 2000,
          disableOnInteraction: false
        },
        speed: 5000
      }
    }
  },
  computed: {
    pages () {
      let pages = []
      this.list.forEach((item, index) => {
        let page = Math.floor(index / 8)
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

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'

  .icons >>> .swiper-container
    height 0
    padding-bottom 50%
  .icons
    margin-top 0.1rem
    .icon
      height 0
      position relative
      overflow hidden
      float left
      width 25%
      padding-bottom 25%
      .icon-img
        position absolute
        top 0
        right 0
        left 0
        bottom 0.44rem
        box-sizing border-box
        padding 0.1rem
        .icon-img-content
          display block
          margin 0 auto
          height 100%
      .icon-desc
        position absolute
        left 0
        right 0
        bottom 0
        height .44rem
        line-height .44rem
        color: $drakTextColor
        text-align center
        ellipsis()
</style>
