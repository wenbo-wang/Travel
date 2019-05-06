<template>
  <div class="header">
    <router-link to="/">
      <span class="iconfont back-icon">&#xe6f5;</span>
    </router-link>
    <h1 class="header-title">城市选择</h1>
  </div>
</template>
<script>
export default {
  name: 'CityHeader'
}
</script>
<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .header
    position relative
    line-height $headerHeight
    background-color $bgColor
    .back-icon
      position absolute
      top 0
      left .1rem
      font-size .4rem
      color #ffffff
    .header-title
      text-align center
      font-size .34rem
      color #ffffff
</style>
