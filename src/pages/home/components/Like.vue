<template>
  <div class="like">
    <div class="like-title">
      <img class="like-title-img" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png">
      <span class="like-title-desc">猜你喜欢</span>
    </div>
    <ul class="like-list">
      <li class="like-item border-bottom" v-for="item of likeList" :key="item.id">
        <div class="like-item-tag">
          {{item.tag}}
        </div>
        <div class="like-item-img">
          <img class="item-img-icon" :src="item.imgUrl">
        </div>
        <div class="like-item-right">
          <div class="item-right-title">{{item.title}}</div>
          <div class="item-right-comment">{{item.comment}}条评论</div>
          <div class="item-right-price">
            <span class="right-price-tag">
              ￥
              <span class="right-price-num">{{item.price}}</span>
            </span>
            起
            <span class="right-price-location">
              {{item.location}}
            </span>
          </div>
          <div class="item-right-desc" v-if="item.desc">{{item.desc}}</div>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeLike',
  data () {
    return {
      likeList: [{
        id: '0001',
        tag: '可订明日',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
        title: '故宫',
        price: '60',
        location: '北京',
        comment: '45',
        desc: '世界五大宫之首'
      }, {
        id: '0002',
        tag: '预约',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
        title: '长城',
        price: '20',
        location: '北京',
        comment: '48'
      }, {
        id: '0003',
        tag: '极速入场',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_250x250_0fc722c0.jpg',
        title: '护城河',
        price: '50',
        location: '西安',
        comment: '50'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .like-title
    position relative
    height .44rem
    padding .24rem 0 .26rem
    .like-title-img
      float left
      display block
      width .3rem
      height .3rem
      margin-left .2rem
    .like-title-desc
      float left
      font-size .32rem
      height .44rem
      line-height .44rem
      margin-left .08rem
      color: #212121
  .like-list
    margin-left .24rem
    .like-item
      position relative
      overflow hidden
      padding .2rem 0
      .like-item-tag
        position absolute
        top .2rem
        left 0
        width 1.02rem
        height .38rem
        font-size .2rem
        line-height .38rem
        text-indent .04rem
        background-size 100%
        background-image:url(https://img1.qunarzz.com/piao/fusion/1802/52/b9080e45b69b4f02.png)
      .like-item-img
        float left
        width 2rem
        height 2rem
        .item-img-icon
          width 100%
      .like-item-right
        padding-left 2.22rem
        .item-right-title
          margin-top .26rem
          height .44rem
          color #212121
          font-size .32rem
          line-height .44rem
        .item-right-comment
          margin-top .14rem
          color #616161
          font-size .24rem
          line-height .34rem
        .item-right-price
          margin-top .22rem
          .right-price-tag
            color #ff8300
            .right-price-num
              font-size .4rem
          .right-price-location
            float right
            margin-right .24rem
            color #616161
            font-size .24rem
            line-height .4rem
        .item-right-desc
          margin-top .48rem
          margin-right .24rem
          font-size .24rem
          line-height .34rem
          color #f55
          background-color #fff9f9
</style>
