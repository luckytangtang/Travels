<template>
<div>
  <city-header></city-header>
  <city-search :cities="cities"></city-search>
  <city-list :cities="cities"
              :hot="hotCities"></city-list>
  <city-alphabet :cities="cities"></city-alphabet>
</div>
</template>

<script>
import axios from 'axios'
import CityHeader from './component/Header'
import CitySearch from './component/Search'
import CityList from './component/List'
import CityAlphabet from './component/Alphabet'
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
      cities: {},
      hotCities: []
    }
  },
  methods: {
    getCityInfo () {
      axios.get('/api/city.json').then(this.getCityInfosucc)
    },
    getCityInfosucc: function (res) {
      console.log(res.data)
      res = res.data
      if (res.data) {
        const data = res.data
        this.cities = data.cities
        this.hotCities = data.hotCities
      }
    }
  },
  mounted () {
    this.getCityInfo()
  }
}
</script>

<style scoped>

</style>
