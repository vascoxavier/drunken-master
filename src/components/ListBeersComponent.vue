<template>
  <div class="columns column-gap is-multiline">
    <beer class="column is-4" v-for="beer in listOfBeers" :beer="beer" :key="beer.id"></beer>
  </div>
</template>
<script>
import BeerComponent from './BeerComponent'
export default {
  props: {
    listOfBeers: Array
  },
  components: {
    'beer': BeerComponent
  },
  data () {
    return ({
      count: [1, 2, 3]
    })
  }
}
</script>
