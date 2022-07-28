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
    <OurClass :cards="cards" />
    <OurStaff />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Carousel from "./components/Carousel.vue";
import CarouselSlide from "./components/CarouselSlide.vue";
import Main from "./components/Main.vue";
import OurClass from "./components/OurClass.vue";
import OurStaff from "./components/OurStaff.vue";
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
          total: 507,
          subject: "Our Pupils",
          description:
            "Praesent interdum est gravida vehicula est node maecenas loareet morbi a dosis luctus novum est praesent.",
        },
        {
          images: require("./assets/images/stroller_alt.png"),
          title: "Congue Gravida",
          text: "Praesent interdum est gravida vehicula est node maecenas loareet morbi a dosis luctus novum est praesent.",
          total: 235,
          subject: "Teaching Hours",
          description:
            "Praesent interdum est gravida vehicula est node maecenas loareet morbi a dosis luctus novum est praesent.",
        },
        {
          images: require("./assets/images/globe_alt.png"),
          title: "Maecenas Node",
          text: "Praesent interdum est gravida vehicula est node maecenas loareet morbi a dosis luctus novum est praesent.",
          total: "100%",
          subject: "Satisfied Parents",
          description:
            "Praesent interdum est gravida vehicula est node maecenas loareet morbi a dosis luctus novum est praesent.",
        },
        {
          images: require("./assets/images/bell_alt.png"),
          title: "Praesent Morbi",
          text: "Praesent interdum est gravida vehicula est node maecenas loareet morbi a dosis luctus novum est praesent.",
          total: 1050,
          subject: "Meals Per Year",
          description:
            "Praesent interdum est gravida vehicula est node maecenas loareet morbi a dosis luctus novum est praesent.",
        },
      ],
      cards: [
        {
          name: "Little Lambs",
          age: "12-24",
          size: "9",
          images: require("./assets/images/class_01-690x506.jpg"),
          title: "Learning&Fun",
          description: "Praesent modea est gravida node vehicula luctus",
          logo: require("./assets/images/toy.png"),
          gallery: require("./assets/images/gallery_01.jpg"),
        },
        {
          name: "Bouncy Bears",
          age: "2-3",
          size: "12",
          images: require("./assets/images/class_01-690x506.jpg"),
          title: "Healthy Meals",
          description: "Praesent modea est gravida node vehicula luctus",
          logo: require("./assets/images/meal.png"),
          gallery: require("./assets/images/gallery_02.jpg"),
        },
        {
          name: "Tenderhearts",
          age: "3-4",
          size: "15",
          images: require("./assets/images/class_01-690x506.jpg"),
          title: "Friendly Place",
          description: "Praesent modea est gravida node vehicula luctus",
          logo: require("./assets/images/school.png"),
          gallery: require("./assets/images/gallery_03.jpg"),
        },
        {
          name: "Shining Stars",
          age: "4-5",
          size: "20",
          images: require("./assets/images/class_01-690x506.jpg"),
          title: "Children Safety",
          description: "Praesent modea est gravida node vehicula luctus",
          logo: require("./assets/images/shield.png"),
          gallery: require("./assets/images/gallery_04.jpg"),
        },
      ],
      teachers: [
        {
          name: " Ruth Richie ",
          role: "Teacher",
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
    OurClass,
    OurStaff,
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
