<template>
  <div id="app">
    <Header :headerLinks="headerLinks" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
/* import Main from "./components/Main.vue.vue" */
/* import Footer from "./components/Footer.vue.vue" */

export default {
  data() {
    return {
      headerLinks: [
        {
          text: "Home",
          images: "./assets/images/home.png",
        },
        {
          text: "Pages",
          images: "./assets/images/document.png",
        },
        {
          text: "Blog",
          images: "./assets/images/home.png",
        },
        {
          text: "Shop",
          images: "./assets/images/home.png",
        },
        {
          text: "Shortcode",
          images: "./assets/images/home.png",
        },
        {
          text: "Support",
          images: "./assets/images/home.png",
        },
        {
          text: "Contact",
          images: "./assets/images/home.png",
        },
      ],
    };
  },
  name: "App",
  components: {
    Header,
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
