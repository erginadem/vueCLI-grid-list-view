<template>
  <div id="app">
      <div class="card card-header">
          <h1 class="text text-dark">Vue Grid/List View</h1>
          <hr />
          <product-list> </product-list>
      </div>
  </div>
</template>

<script>
    import ProductList from './components/ProductList.vue'

    export default {
        name: 'app',

        components: {
            ProductList
        }
    }
</script>


<style lang="scss">

</style>
