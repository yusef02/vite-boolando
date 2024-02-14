<script>
import AppLogo from "./AppLogo.vue";
import AppNav from "./AppNav.vue";

export default {
  data() {
    return {
      headerNavSections: [
        { src: "#", tagText: "Donna" },
        { src: "#", tagText: "Uomo" },
        { src: "#", tagText: "Bambini" },
      ],
      headerNavLinkto: [
        {
          src: "#",
          tagIcon: {
            solid: false,
            regular: true,
            brand: false,
            icon: "fa-user",
          },
        },
        {
          src: "#",
          tagIcon: {
            solid: false,
            regular: true,
            brand: false,
            icon: "fa-heart",
          },
        },
        {
          src: "#",
          tagIcon: {
            solid: true,
            regular: false,
            brand: false,
            icon: "fa-bag-shopping",
          },
        },
      ],
    };
  },

  components: { AppLogo, AppNav },
  mounted() {
    console.log("AppHeader mounted");
  },
};
</script>
<template>
  <header class="header">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-md">
          <app-nav :navLinks="headerNavSections"></app-nav>
        </div>
        <div class="col-md">
          <app-logo></app-logo>
        </div>
        <div class="col-md">
          <app-nav :navIcons="headerNavLinkto"></app-nav>
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
  .col-md {
    flex: 0 0 0;
  }
  .col-md:nth-child(2) {
    flex-grow: 1;
    img {
      height: 50px;
    }
  }
}
</style>
