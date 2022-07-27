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
  data: function () {
    return {
      headerLinks: [
        {
          text: "Home",
          images: require("./assets/home.png"),
        },
        {
          text: "Pages",
          images: require("./assets/document.png"),
        },
        {
          text: "Blog",
          images: require("./assets/printer.png"),
        },
        {
          text: "Shop",
          images: require("./assets/cart.png"),
        },
        {
          text: "Shortcode",
          images: require("./assets/lab.png"),
        },
        {
          text: "Support",
          images: require("./assets/chat.png"),
        },
        {
          text: "Contact",
          images: require("./assets/envelope.png"),
        },
      ],
      /* headerSlides: [
        "./assets/images/slider_slide1_background.png",
        "./assets/images/slider_slide1_background.png",
        "./assets/images/slider_slide1_background.png",
      ], */
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
