<script>
export default {
  data() {
    return {
      title: "boolean logo",
      img: "boolean-logo.png",
    };
  },
  methods: {
    buildImagePath(image) {
      return new URL("../assets/img/" + image, import.meta.url).href;
    },
  },
};
</script>
<template>
  <img :src="buildImagePath(img)" :alt="title" />
</template>
<style></style>
