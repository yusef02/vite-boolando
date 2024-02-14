<script>
import { store } from "../store";
import axios from "axios";

import AppArticleProduct from "./AppArticleProduct.vue";
export default {
  data() {
    return {
      store,
      articles: [],
    };
  },
  components: { AppArticleProduct },
  created() {
    axios.get(`${store.apiUri}/products`).then((res) => {
      this.articles = res.data;
    });
  },
};
</script>
<template>
  <main>
    <div class="container">
      <div class="row gy-4">
        <app-article-product
          v-for="article in articles"
          :product="article"
        ></app-article-product>
      </div>
    </div>
  </main>
</template>
<style lang="scss">
main {
  padding: 40px 0;
  .row {
    flex-direction: row;
    flex-wrap: wrap;
  }
}
</style>
