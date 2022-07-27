<template>
  <div id="app">
    <Header :headerLinks="headerLinks" />
    <carousel @next="next" @prev="prev">
      <carousel-slide
        v-for="(slide, index) in slides"
        :key="slide"
        :index="index"
        :visibleSlide="visibleSlide"
      >
        <img class="sliderImages" :src="slide" />
      </carousel-slide>
    </carousel>
    <Main :mainInfos="mainInfos" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Carousel from "./components/Carousel.vue";
import CarouselSlide from "./components/CarouselSlide.vue";
import Main from "./components/Main.vue";
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
      slides: [
        require("./assets/images/slider_slide1_background.png"),
        require("./assets/images/slider_slide2_background.png"),
        require("./assets/images/slider_slide3_background.png"),
      ],
      visibleSlide: 0,

      mainInfos: [
        {
          images: require("./assets/images/schoolbag_alt.png"),
          title: "Morbi Etos",
          text: "Praesent interdum est gravida vehicula est node maecenas loareet morbi a dosis luctus novum est praesent.",
        },
        {
          images: require("./assets/images/bell_alt.png"),
          title: "Morbi Etos",
          text: "Praesent interdum est gravida vehicula est node maecenas loareet morbi a dosis luctus novum est praesent.",
        },
        {
          images: require("./assets/images/bell_alt.png"),
          title: "Morbi Etos",
          text: "Praesent interdum est gravida vehicula est node maecenas loareet morbi a dosis luctus novum est praesent.",
        },
        {
          images: require("./assets/images/bell_alt.png"),
          title: "Morbi Etos",
          text: "Praesent interdum est gravida vehicula est node maecenas loareet morbi a dosis luctus novum est praesent.",
        },
      ],
    };
  },
  computed: {
    slideLen() {
      return this.slides.length;
    },
  },
  methods: {
    next() {
      if (this.visibleSlide >= this.slidesLen - 1) {
        this.visibleSlide = 0;
      } else {
        this.visibleSlide++;
      }
    },
    prev() {
      if (this.visibleSlide <= 0) {
        this.visibleSlide = this.slidesLen - 1;
      } else {
        this.visibleSlide--;
      }
    },
  },
  name: "App",
  components: {
    Header,
    Carousel,
    CarouselSlide,
    Main,
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.sliderImages {
  width: 100%;
}
</style>
