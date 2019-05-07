<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
  </div>
</template>
<script>
import CityHeader from './components/Header'
import CitySearch from './components/Search'
import axios from 'axios'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch
  },
  data () {
    return {

    }
  },
  methods: {
    getCityInfo () {
      axios.get('api/city.json').then(
        this.getCityInfoSucc
      )
    },
    getCityInfoSucc: function (res) {
      // todo 处理数据
    }
  },
  mounted () {
    this.getCityInfo()
  }
}
</script>
