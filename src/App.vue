<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  data() {
    return {
      title: "My Vue project",
    };
  },
  components: { AppHeader, AppMain, AppFooter },
  mounted() {
    console.log("AppVue mounted");
  },
};
</script>
<template>
  <app-header></app-header>
  <app-main></app-main>
  <app-footer></app-footer>
</template>
<style lang="scss">
@use "./assets/style/general.scss" as *;
</style>
