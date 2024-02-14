<script>
import LikeButton from "./LikeButton.vue";
export default {
  data() {
    return {};
  },
  props: ["product"],
  components: { LikeButton },
  methods: {
    buildImagePath(image) {
      return new URL("../assets/img/" + image, import.meta.url).href;
    },
  },
};
</script>
<template>
  <div class="col-md-4">
    <div class="card article">
      <like-button :isLike="product.liked"></like-button>
      <img :src="buildImagePath(product.img1)" :alt="product.img" />
      <img :src="buildImagePath(product.img2)" :alt="product.img" />
      <div class="tagged">
        <span v-if="product.badges.sale" class="sale">{{
          product.badges.sale
        }}</span>
        <span v-if="product.badges.sustainability" class="sostenibile"
          >sostenibile</span
        >
      </div>
      <div class="article--desc">
        <p class="">{{ product.desc.brand }}</p>
        <p>
          <strong>{{ product.desc.model }}</strong>
        </p>
        <span class="current-price"
          ><strong>{{ product.desc.currentPrice }} &euro;</strong></span
        >
        <span v-if="product.desc.previousPrice" class="previous-price"
          >{{ product.desc.previousPrice }} &euro;</span
        >
      </div>
    </div>
  </div>
</template>
<style lang="scss">
.article {
  position: relative;
  padding: 10px;

  .sale {
    color: white;
    background-color: red;
    padding: 2px 5px;
    margin-right: 3px;
  }
  .sostenibile {
    color: white;
    background-color: green;
    padding: 2px 5px;
  }
}

.article .tagged {
  position: absolute;
  top: 80%;
}

/* descrizione articolo */
.article .article--desc span {
  display: inline-block;
  margin-right: 0.5rem;
}

.article .article--desc .current-price {
  color: red;
}

.article .article--desc .previous-price {
  color: rgb(68, 68, 68);
  text-decoration: line-through;
}
.article img:last-of-type {
  display: none;
}
.article:hover img:first-of-type {
  display: none;
}
.article:hover img:last-of-type {
  display: block;
}
</style>
