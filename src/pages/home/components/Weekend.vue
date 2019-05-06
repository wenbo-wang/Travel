<template>
  <div class="weekend">
    <h2 class="weekend-title">周末去哪儿</h2>
    <div>
      <div class="weekend-item" v-for="item of weekendList" :key="item.id">
        <div class="weekend-item-img">
          <img class="item-img-icon" :src="item.imgUrl">
        </div>
        <div class="weekend-item-content">
          <p class="item-content-name">{{item.name}}</p>
          <p class="item-content-desc">{{item.desc}}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      weekendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1603/6d/2f67ae0659f41f.jpg_r_640x214_bf6cbd0b.jpg',
        name: '北京赏花好地方',
        desc: '乱花渐欲迷人眼，京城赏花大搜索'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1603/6d/2f67ae0659f41f.jpg_r_640x214_bf6cbd0b.jpg',
        name: '北京赏花好地方',
        desc: '乱花渐欲迷人眼，京城赏花大搜索'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1603/6d/2f67ae0659f41f.jpg_r_640x214_bf6cbd0b.jpg',
        name: '北京赏花好地方',
        desc: '乱花渐欲迷人眼，京城赏花大搜索'
      }]
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
