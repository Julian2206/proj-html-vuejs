<template>
  <section>
    <div class="carousel">
      <slot></slot>

      <button @click="next" class="next">Next</button>
      <button @click="prev" class="prev">Prev</button>
    </div>
    <div class="headerInfo">
      <h2>How to Enroll Your Child to a Class?</h2>
      <button>Learn More</button>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    next() {
      this.$emit("next");
    },
    prev() {
      this.$emit("prev");
    },
  },
};
</script>

<style>
.carousel {
  position: relative;
  width: 100%;
  height: 650px;
  overflow: hidden;
}
.carousel button {
  position: absolute;
  height: 40px;
  width: 50px;
  top: calc(50% - 20px);
  background-color: rgba(0, 0, 0, 0.8);
  border: none;
  color: #fff;
}
.carousel button:focus-visible,
.carousel button:hover {
  /* outline: none; */
  cursor: pointer;
}
.next {
  right: 0;
}
.prev {
  left: 0;
}

.headerInfo {
  background-image: url("../assets/images/pattern.png");
  display: flex;
  justify-content: space-around;
  align-items: center;
  height: 100px;
}
.headerInfo h2 {
  color: #fff;
  font-size: 30px;
}
.headerInfo button {
  height: 40px;
  width: 100px;
  font-size: 14px;
  background-color: #554e9e;
  color: #fff;
  border: 1px solid #fff;
}
.headerInfo button:hover {
  cursor: pointer;
  background-color: #fff;
  color: black;
}
</style>
