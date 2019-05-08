<template>
  <div class="search">
    <div class="input-wrapper">
      <input class="search-input" type="text" placeholder="输入城市名或拼音" v-model="keywords">
    </div>
    <div class="search-content" ref="content" v-show="this.keywords">
      <ul>
        <li class="search-item border-bottom" v-for="item of list" :key="item.id">{{item.name}}</li>
        <li class="search-item border-bottom" v-show="hasData">没有匹配到结果</li>
      </ul>
    </div>
  </div>
</template>
<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CitySearch',
  props: {
    cities: Object
  },
  data () {
    return {
      keywords: '',
      list: [],
      timer: null
    }
  },
  computed: {
    hasData () {
      return !this.list.length
    }
  },
  watch: {
    keywords () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keywords) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((value) => {
            if (value.name.indexOf(this.keywords) > -1 || value.spell.indexOf(this.keywords) > -1) {
              result.push(value)
            }
          })
        }
        this.list = result
      })
    }
  },
  mounted () {
    console.log(this.$refs.content)
    this.scroll = new Bscroll(this.$refs.content)
  }
}
</script>
<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .search
    .input-wrapper
      height .72rem
      padding 0 .1rem
      background-color $bgColor
      .search-input
        box-sizing border-box
        width 100%
        height .62rem
        line-height .62rem
        border-radius .1rem
        text-align center
        color #666
        padding 0 .1rem
    .search-content
      overflow hidden
      z-index 1
      position absolute;
      top 1.56rem
      left 0
      right 0
      bottom 0
      background-color #eee
      .search-item
        line-height .62rem
        padding-left .2rem
        background-color #ffffff
</style>
