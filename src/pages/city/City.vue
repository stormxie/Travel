<template>
    <div>
        <city-header></city-header>
        <city-search></city-search>
        <city-list></city-list>
    </div>
</template>

<script>
import CityAlphabet from './components/Alphabet'
import CityHeader from './components/Header'
import CityList from './components/List'
import CitySearch from './components/Search'

export default {
  name: 'City',
  components: {
    CityAlphabet,
    CityHeader,
    CityList,
    CitySearch
  },
  data () {
    return {}
  }
}
</script>
