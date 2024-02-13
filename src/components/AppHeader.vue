<script>
import AppLogo from "./AppLogo.vue";
export default {
  data() {
    return {
      headerNavSections: [
        { src: "#Donna", tagText: "Donna" },
        { src: "#Uomo", tagText: "Uomo" },
        { src: "#Bambini", tagText: "Bambini" },
      ],
      headerNavLinkto: [
        { src: "#", tag: "Donna" },
        { src: "#", tag: "Uomo" },
        { src: "#", tag: "Bambini" },
      ],
    };
  },

  components: { AppLogo },
  mounted() {
    console.log("AppHeader mounted");
  },
};
</script>
<template>
  <header class="header">
    <div class="container">
      <div class="row align-items-center">
        <div class="col header__nav">
          <ul>
            <li v-for="tag in headerNavSections">
              <a :href="tag.src">{{ tag.tagText }}</a>
            </li>
          </ul>
        </div>
        <div class="col">
          <app-logo></app-logo>
        </div>
        <div class="col header__nav">
          <ul>
            <li v-for="tag in headerNavLinkto">
              <a :href="tag.src">{{ tag.tag }}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>
<style lang="scss">
.header {
  padding: 10px 0;
  color: white;
  background-color: #ff6900;
  position: sticky;
  top: 0;
  z-index: 1;
  text-align: center;

  &__nav {
    flex: 0 0 0;
    ul {
      list-style: none;
      padding: 0;
      margin: 0;
      display: flex;
      flex-direction: row;

      li {
        padding: 1rem 1.5rem;
        a {
          text-decoration: none;
          color: white;
        }
      }
    }
  }
  .col:nth-child(2) img {
    height: 50px;
    flex-grow: 1;
  }
}
</style>
