<script>
import AppHeader from "./components/AppHeader.vue";
import EmptyContent from "./components/EmptyContent.vue";

export default {
  data() {
    return {

    }
  },

  components: {
    AppHeader,
    EmptyContent,
  }
}

</script>

<template>
  <AppHeader />
  <EmptyContent />
</template>

<style lang="scss">
@use "./styles/general.scss";
</style>
