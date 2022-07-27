<template>
  <header class="header">
    <div class="container">
      <div class="navbar">
        <div class="logo">
          <img src="../assets/images/logo.png" alt="" />
        </div>
        <div>
          <ul>
            <li v-for="headerLink in headerLinks" v-bind:key="headerLink.id">
              <img class="navLinks" :src="headerLink.images" />
              {{ headerLink.text }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    headerLinks: Array,
    images: Object,
  },
};
</script>

<style lang="scss">
.header {
  width: 100%;
  height: 250px;
  background-color: #fefffe;
}

.logo img {
  width: 160px;
  height: 120px;
}

.navbar {
  width: 100%;
  height: 200px;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.navbar ul {
  display: flex;
  justify-content: center;
  list-style: none;
  margin-top: 40px;
}

.navbar ul li {
  width: 60px;
  padding: 80px;
}
</style>
