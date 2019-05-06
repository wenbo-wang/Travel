<template>
  <div class="hot">
    <div class="hot-title">
      <img class="hot-title-img" src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png">
      <span class="hot-title-desc">本周热门榜单</span>
      <div class="hot-title-all">
        <span>全部榜单</span>
        <span class="iconfont">&#xe6f3;</span>
      </div>
    </div>
    <ul class="hot-list">
      <li class="hot-list-item" v-for="item of hotList" :key="item.id">
        <div class="hot-list-item-full">
          <div class="item-full-tag" v-if="item.tagUrl">
            <img class="item-full-tag-img" :src="item.tagUrl">
          </div>
          <div class="item-full-img">
            <img class="full-img-icon" :src="item.imgUrl">
          </div>
          <div class="item-full-desc">{{item.desc}}</div>
          <div class="item-full-price">
            <span class="price-tag">
              ￥
              <em class="price-num">{{item.price}}</em>
            </span>
            起
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeHotSale',
  props: {
    hotList: Array
  },
  data () {
    return {
    }
  }
}
</script>
<style lang="stylus" scoped>
  .hot-title
    position relative
    height .44rem
    padding .24rem 0 .26rem
    .hot-title-img
      float left
      display block
      width .3rem
      height .3rem
      margin-left .2rem
    .hot-title-desc
      float left
      font-size .32rem
      height .44rem
      line-height .44rem
      margin-left .08rem
      color: #212121
    .hot-title-all
      float right
  .hot-list
    overflow-x auto
    white-space nowrap;
    padding 0 .14rem 0 .24rem
    .hot-list-item
      display: inline-block
      width 2rem
      margin-right .1rem
      margin-bottom .2rem
      .hot-list-item-full
        width 100%
        height 100%
        position relative
        .item-full-tag
          position absolute
          top 0
          left 0
          width .84rem
          height .4rem
          .item-full-tag-img
            width 100%
        .item-full-img
          overflow hidden
          width 2rem
          height 0
          padding-bottom 100%
          .full-img-icon
            width 100%
        .item-full-desc
          margin-top .12rem
          height .32rem
          line-height .32rem
          text-align center
          color #212121
        .item-full-price
          height .36rem
          color #616161
          margin-top .1rem
          text-align center
          .price-tag
            color #ff8300
            .price-num
              font-size .28rem
</style>
