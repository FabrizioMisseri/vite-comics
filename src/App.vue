<script>
import AppHeader from "./components/AppHeader.vue";
import AppNavbar from "./components/AppNavbar.vue";

export default {
  data() {
    return {

    }
  },

  components: {
    AppHeader,
    AppNavbar
  }
}

</script>

<template>
  <AppHeader />
  <AppNavbar />
</template>

<style lang="scss">
@use "./styles/general.scss";
</style>
