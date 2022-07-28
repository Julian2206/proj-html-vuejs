<template>
  <main>
    <div class="mainSectionHeader">
      <h1>Welcome to Fable</h1>
      <h4>Fable daycare, preschool, and kindergarten</h4>
      <img src="../assets/images/header_divider.png" alt="header divider" />
    </div>

    <div class="mainInfoContainer">
      <ul>
        <li class="mainList" v-for="(mainInfo, id) in mainInfos" :key="id">
          <!-- todo set different color -->
          <img class="main-logo" v-bind:src="mainInfo.images" />
          <h3>{{ mainInfo.title }}</h3>
          <p>{{ mainInfo.text }}</p>
        </li>
      </ul>
    </div>

    <div class="mainOverviewContainer">
      <div class="mainOverviewLeft">
        <button class="btn-overview">Overview</button>
        <button class="btn-mission">Our Mission</button>
        <h3>
          Our philosophy is learning through play as we offer a stimulating
          envinroment for children.
        </h3>
        <div class="day-section">
          <img src="../assets/images/clock_alt.png" alt="clock" />
          <div>
            <h4>Full Day Session</h4>
            <p>
              Pulvinar est metro ligula blandit maecenas retrum gravida cuprum.
              Maecenas estibulum
            </p>
          </div>
        </div>
        <div class="varied-class">
          <img src="../assets/images/diagram_alt.png" alt="" />
          <div>
            <h4>Varied Classes</h4>
            <p>
              Pulvinar est metro ligula blandit maecenas retrum gravida cuprum.
              Maecenas estibulum
            </p>
          </div>
        </div>
      </div>

      <div class="mainOverviewRight">
        <img src="../assets/images/gallery_01-690x506.jpg" alt="" />
      </div>
    </div>

    <div class="mainFooterContainer">
      <ul>
        <li
          class="mainFooterList"
          v-for="(mainInfo, id) in mainInfos"
          :key="id"
        >
          <h2>{{ mainInfo.total }}</h2>
          <h3>{{ mainInfo.subject }}</h3>
          <p>{{ mainInfo.description }}</p>
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
  font-size: 50px;
  color: #554e9e;
  padding: 10px;
}
.mainSectionHeader h4 {
  color: grey;
  padding: 10px;
}
.mainSectionHeader img {
  margin-top: 20px;
  margin-bottom: 30px;
}

.mainInfoContainer {
  width: 100%;
  height: 400px;
  text-align: center;
}

.mainInfoContainer ul {
  display: flex;
  justify-content: center;
  width: 100%;
}

.mainInfoContainer ul li {
  width: calc(60% / 4);
  height: 200px;
  display: flex;
  align-items: center;
  flex-direction: column;
}
.mainInfoContainer ul li img {
  width: 120px;
  height: 160px;
  background-color: #fe6601;
  border-radius: 50%;
  padding: 30px;
  margin-bottom: 15px;
}
.mainInfoContainer ul li h3 {
  color: #554e9e;
  margin-bottom: 20px;
}
.mainInfoContainer ul li p {
  color: darkgrey;
  margin-bottom: 20px;
}
/* overview */
.mainOverviewContainer {
  width: 100%;
  height: auto;
  display: flex;
  justify-content: center;
  background-color: #e8e6e7;
  padding: 60px;
}

.mainOverviewLeft {
  width: 50%;
}
.mainOverviewLeft .btn-overview {
  width: 130px;
  font-size: 20px;
  padding: 10px;
  border-color: #fe6601;
  color: white;
  background-color: #fe6601;
  margin-bottom: 40px;
}

.mainOverviewLeft .btn-mission {
  font-size: 20px;
  padding: 10px;
  color: grey;
  margin-left: 15px;
  margin-bottom: 40px;
}

.mainOverviewLeft h3 {
  font-size: 30px;
  color: #554e9e;
  margin-bottom: 35px;
}

.mainOverviewLeft img {
  background-color: #fe6601;
  border-radius: 50%;
  width: 80px;
  height: 80px;
  padding: 20px;
}

.mainOverviewLeft .day-section {
  display: flex;
  margin-bottom: 40px;
}

.mainOverviewLeft .varied-class {
  display: flex;
  margin-bottom: 40px;
}

.day-section img {
  margin-right: 25px;
}
.day-section h4 {
  color: #554e9e;
  font-size: 25px;
  margin-bottom: 15px;
}
.day-section p {
  color: grey;
  font-size: 20px;
  overflow: hidden;
}

.varied-class img {
  margin-right: 25px;
}
.varied-class h4 {
  color: #554e9e;
  font-size: 25px;
  margin-bottom: 15px;
}
.varied-class p {
  color: grey;
  font-size: 20px;
  overflow: hidden;
}
/* main-footer */
.mainFooterContainer {
  width: 100%;
  height: 500px;

  background-image: url("../assets/images/parallax_01.jpg");
}

.mainFooterContainer ul {
  display: flex;
  justify-content: center;
  width: 100%;
  list-style: none;
}
.mainFooterContainer ul li {
  width: calc(60% / 4);
  height: 350px;
  display: flex;
  justify-content: space-around;
  padding: 20px;
  align-items: center;
  flex-direction: column;
  text-align: center;
}
.mainFooterContainer ul li h2 {
  width: 160px;
  height: 160px;
  background-color: rgba(0, 0, 0, 0.1);
  border: 1px solid white;
  color: white;
  font-size: 40px;
  border-radius: 50%;
  padding: 40px;
  margin-top: 35px;
  margin-bottom: 15px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
