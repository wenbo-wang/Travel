<template>
  <div class="weekend">
    <h2 class="weekend-title">周末去哪儿</h2>
    <div>
      <div class="weekend-item" v-for="item of weekendList" :key="item.id">
        <div class="weekend-item-img">
          <img class="item-img-icon" :src="item.imgUrl">
        </div>
        <div class="weekend-item-content">
          <p class="item-content-name">{{item.title}}</p>
          <p class="item-content-desc">{{item.desc}}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeWeekend',
  props: {
    weekendList: Array
  },
  data () {
    return {
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .weekend
    margin-top .1rem
    .weekend-title
      font-size .32rem
      height .8rem
      line-height .8rem
      margin-left .32rem
      color #212121
    .weekend-item
      margin-bottom .1rem
      .weekend-item-img
        overflow hidden
        height 0
        padding-bottom 38.9%
        .item-img-icon
          width 100%
      .weekend-item-content
        padding .14rem .2rem .2rem .2rem
        .item-content-name
          font-size .28rem
          line-height .48rem
          padding-left .2rem
          ellipsis()
        .item-content-desc
          font-size .24rem
          line-height .48rem
          padding-left .2rem
          ellipsis()
</style>
