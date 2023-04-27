<template>
  <div @click="removeMenusHandler($event)">
    <AppHeader />
    <AppMain />
  </div>
</template>

<script>
  import { removeMenusHandler } from "./assets/menu.js";
  import AppHeader from "./components/AppHeader.vue";
  import AppMain from "./components/AppMain.vue";

  export default {
    name: "App",
    
    components: {
      AppHeader,
      AppMain
    },

    methods: {
      removeMenusHandler: removeMenusHandler
    },
  }
</script>

<style lang="scss" scoped>

</style>