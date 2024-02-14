<script>
import AppNav from "./AppNav.vue";
export default {
  data() {
    return {
      title: "Boolando s.r.l.",
      footerInfo: [
        { src: "#", tagText: "Informazioni legali" },
        { src: "#", tagText: "Informativa sulla privacy" },
        { src: "#", tagText: "Diritto di recesso" },
      ],
      footerSocials: [
        {
          src: "#",
          tagIcon: {
            solid: false,
            regular: false,
            brand: true,
            icon: "fa-square-twitter",
          },
        },
        {
          src: "#",
          tagIcon: {
            solid: false,
            regular: false,
            brand: true,
            icon: "fa-square-facebook",
          },
        },
        {
          src: "#",
          tagIcon: {
            solid: false,
            regular: false,
            brand: true,
            icon: "fa-square-instagram",
          },
        },
        {
          src: "#",
          tagIcon: {
            solid: false,
            regular: false,
            brand: true,
            icon: "fa-square-pinterest",
          },
        },
        {
          src: "#",
          tagIcon: {
            solid: false,
            regular: false,
            brand: true,
            icon: "fa-square-youtube",
          },
        },
      ],
    };
  },
  components: { AppNav },
};
</script>
<template>
  <footer class="footer">
    <div class="container">
      <div class="row">
        <div class="col-md footer__info">
          <h1>{{ title }}</h1>
          <app-nav :navLinks="footerInfo"></app-nav>
        </div>
        <div class="col-md footer__socials">
          <span class="small">Trovaci anche su</span><br />
          <app-nav :navIcons="footerSocials"></app-nav>
        </div>
      </div>
    </div>
  </footer>
</template>
<style lang="scss">
.footer {
  background-color: #1a1a1a;
  height: 100px;
  color: white;
  padding: 30px 0;

  h1 {
    font-size: 1.2rem;
  }
}
</style>
