<script>
import { store } from "../store";

export default {
  data() {
    return {
      store,
    };
  },
  methods: {
    buildImagePath(image) {
      return new URL("../assets/img/" + image, import.meta.url).href;
    },
  },
  created() {
    console.log(this.store);
  },
};
</script>
<template>
  <img :src="buildImagePath(store.logo)" :alt="title" />
</template>
<style></style>
