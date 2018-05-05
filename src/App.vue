<template>
  <div class="tiles is-ancestor">
    <div class="tiles is-vertical is-12">
      <navbar></navbar>
    </div>
    <div class="tile is-child is-vertical is-offset-4 is-4">
      <search-beer></search-beer>
    </div>
    <list-beers :listOfBeers="getBeers"></list-beers>
  </div>
</template>

<script>
import NavbarComponent from './components/NavbarComponent'
import SearchBeerComponent from './components/SearchBeerComponent'
import ListBeersComponent from './components/ListBeersComponent'

let axios = require('axios')

export default {
  name: 'App',
  data () {
    return (
      {
        listOfBeers: []
      }
    )
  },
  components: {
    'navbar': NavbarComponent,
    'search-beer': SearchBeerComponent,
    'list-beers': ListBeersComponent
  },
  computed: {
    getBeers () {
      return this.listOfBeers
    }
  },
  mounted () {
    const URL = 'https://api.punkapi.com/v2/beers?page=1&per_page=12'
    let data = this
    axios
      .get(URL)
      .then(function (response) { data.listOfBeers = response.data })
  }
}
</script>

<style>

</style>
