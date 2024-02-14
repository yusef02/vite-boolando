<script>
import axios from "axios";
import { store } from "../store";

export default {
  data() {
    return {};
  },
  props: ["isLike"],
  methods: {
    clickLike() {
      axios.post(`${store.apiUri}/products`).then((ask) => {
        console.log(ask.data);
        // ask.data = isLike;
      });
    },
  },
  created() {
    console.log(this.isLike);
  },
};
</script>
<template>
  <button class="article--like-btn btn" @click="clickLike()">&hearts;</button>
</template>
<style lang="scss">
.article .article--like-btn {
  display: inline-block;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 3rem;
  height: 3rem;
  font-size: 1.5rem;
  line-height: 3rem;
  text-align: center;
  vertical-align: middle;
  background-color: lightgrey;
  position: absolute;
  top: 10px;
  right: 10px;
}
</style>
