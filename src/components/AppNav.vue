<script>
export default {
  data() {
    return {};
  },
  props: { navLinks: Array, navIcons: Array },
  created() {
    console.log(this.navLinks);
  },
};
</script>
<template>
  <div class="nav">
    <ul>
      <li v-show="navLinks" v-for="tag in navLinks">
        <a :href="tag.src">{{ tag.tagText }}</a>
      </li>
      <li v-show="navIcons" v-for="tag in navIcons">
        <a :href="tag.src"
          ><i
            :class="[
              tag.tagIcon.icon,
              {
                'fa-solid': tag.tagIcon.solid,
                'fa-regular': tag.tagIcon.regular,
                'fa-brands': tag.tagIcon.brand,
              },
            ]"
          ></i
        ></a>
      </li>
    </ul>
  </div>
</template>
<style lang="scss">
.nav {
  ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    flex-direction: row;
    gap: 0.7rem;
    li {
      a {
        text-decoration: none;
        color: white;
      }
    }
  }
}
</style>
