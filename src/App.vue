<script>
import AppHeader from "./components/AppHeader.vue";
import ProductList from "./components/ProductList.vue";

export default {
  data() {
    return {

    }
  },

  components: {
    AppHeader,
    ProductList,
  }
}

</script>

<template>
  <AppHeader />
  <ProductList />
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
