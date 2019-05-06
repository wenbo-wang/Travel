<template>
  <div class="icons">
    <swiper :options="swiperOption" v-if="showSwiper">
      <!-- slides -->
      <swiper-slide v-for = '(page, index) of pages' :key="index">
          <div class="icon"  v-for="item of page" :key="item.id">
            <div class="icon-img">
              <img class="icon-img-content" :src="item.imgUrl">
            </div>
            <p class="icon-desc">{{item.desc}}</p>
          </div>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeIcons',
  props: {
    iconList: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    },
    showSwiper () {
      return this.iconList.length
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .icons
    padding-top .1rem
  .icons >>> .swiper-container
    height 0
    padding-bottom 55%
  .icons >>> .swiper-pagination-bullet-active
    background rgba(0,175,190,.8) !important
  .icon
    position relative
    overflow hidden
    height 0
    float left
    width 25%
    padding-bottom 25%
    .icon-img
      width 1.1rem
      height 1.1rem
      margin 0 auto
      .icon-img-content
        width 100%
    .icon-desc
      height .44rem
      line-height .44rem
      margin-top .1rem
      text-align center
      font-size .28rem
      ellipsis()
</style>
