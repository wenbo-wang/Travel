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
      <li class="hot-list-item">ceshi</li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeHotSale'
}
</script>
<style lang="stylus" scoped>
  .hot
    height  3.6rem
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
      overflow-x scroll
      padding 0 .24rem
      .hot-list-item
        float left
        width 2rem
</style>
