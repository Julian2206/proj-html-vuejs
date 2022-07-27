<template>
  <main>
    <div class="mainSectionHeader">
      <h1>Welcome to Fable</h1>
      <h4>Fable daycare, preschool, and kindergarten</h4>
      <img src="../assets/images/header_divider.png" alt="header divider" />
    </div>
    <div>
      <ul>
        <li v-for="(mainInfo, id) in mainInfos" :key="id">
          <img class="main-logo" v-bind:src="mainInfo.images" />
          {{ mainInfo.title }} {{ mainInfo.text }}
        </li>
      </ul>
    </div>
  </main>
</template>

<script>
export default {
  props: {
    mainInfos: Array,
  },
};
</script>

<style lang="scss">
.mainSectionHeader {
  text-align: center;
  padding: 20px;
}
.mainSectionHeader h1 {
  color: #554e9e;
  padding: 10px;
}
.mainSectionHeader h4 {
  color: grey;
  padding: 10px;
}
.mainSectionHeader img {
  margin-top: 20px;
}
</style>
