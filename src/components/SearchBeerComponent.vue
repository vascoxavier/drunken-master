<template>
    <div class="field level">
      <label class="label">Search beer:</label>
      <input class="input is-rounded Large" type="text" :placeholder="placeholder">
    </div>
</template>

<script>
export default {
  name: 'search-beer',
  data () {
    return ({
      placeholder: 'Digite o nome da cerveja que estas a procurar aqui'
    })
  }
}
</script>

<style>

</style>
