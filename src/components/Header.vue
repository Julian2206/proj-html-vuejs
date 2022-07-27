<template>
  <header class="header">
    <div class="container">
      <div class="navbar">
        <div class="logo">
          <img src="../assets/images/logo.png" alt="logo" />
        </div>
        <div>
          <ul>
            <a
              href="#"
              v-for="headerLink in headerLinks"
              v-bind:key="headerLink.id"
            >
              <img class="navLinksImages" v-bind:src="headerLink.images" />
              {{ headerLink.text }}
            </a>
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
  },
};
</script>

<style lang="scss">
.header {
  width: 100%;
  height: 200px;
  background-color: #fefffe;
  /* background-color: aqua; */
}

.logo img {
  width: 160px;
  height: 120px;
  margin-top: 40px;
  margin-left: 30px;
}

.navbar {
  width: 100%;
  height: 150px;
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

.navbar ul a {
  width: 60px;
  padding: 80px;
  text-decoration: none;
}

.navbar ul a:hover {
  background-color: #fe6601;
}
</style>
