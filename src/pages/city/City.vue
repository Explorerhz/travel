<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list :hotCities="hotCities" :cities="cities"></city-list>
    <city-alphabet :cities="cities"></city-alphabet>
  </div>
</template>
<script>
import CityHeader from './components/Header'
import CitySearch from './components/Search'
import CityList from './components/List'
import CityAlphabet from './components/Alphabet'
import axios from 'axios'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphabet
  },
  data () {
    return {
      hotCities: [],
      cities: {}
    }
  },
  mounted () {
    axios.get('/api/city.json')
      .then(this.getCityInfo)
  },
  methods: {
    getCityInfo (res) {
      console.log(res)
      var data = res.data.data
      this.hotCities = data.hotCities
      this.cities = data.cities
    }
  }
}
</script>
<style lang="stylus" scoped>

</style>
