<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe6f5;</span>
    </div>
    <div class="header-center">
      <span class="iconfont">&#xe705;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      {{this.city}}
      <span class="iconfont">&#xe625;</span>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>
<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .header
    display flex
    line-height .86rem
    background-color $bgColor
    color #ffffff
    .header-left
      width .64rem
      float left
      text-align center
      .back-icon
        font-size .4rem
    .header-center
      flex 1
      height .64rem
      line-height .64rem
      background-color #ffffff
      border-radius .1rem
      margin-top .12rem
      margin-left .12rem
      padding-left .2rem
      color #ccc
    .header-right
      width 1.24rem
      float right
      text-align center
</style>
