<template>
  <section>
    <div class="our-class-header">
      <h1>Our Classes</h1>
      <h4>Our preschool program has four dedicated class</h4>
      <img src="../assets/images/header_divider.png" alt="header divider" />
      <div class="our-class-info">
        <h4>
          We provided four classes with nine to twenty children each aged twelve
          month to five years of age.
        </h4>
        <p>
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorem, sit
          qui. Omnis obcaecati illo at reiciendis delectus culpa nulla quod
          quae, adipisci aspernatur enim sapiente aperiam hic! Optio, iste
          expedita.
        </p>
      </div>
      <div class="card-container">
        <div class="card" v-for="(card, i) in cards" :key="i">
          <div class="card-info">
            <h4>{{ card.name }}</h4>
            <br />Class name
            <p>{{ card.age }}</p>
            <br />Month olds
            <p>{{ card.size }}</p>
            <br />Class size
            <div class="card-image">
              <img :src="card.images" alt="" />
              <button>READ MORE</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    cards: Array,
  },
};
</script>

<style lang="scss">
.our-class-header {
  width: 100%;
  height: auto;
  padding: 20px;
  text-align: center;
}
.our-class-header h1 {
  font-size: 50px;
  color: #554e9e;
  padding: 10px;
}
.our-class-header > h4 {
  color: grey;
  padding: 10px;
  font-size: 18px;
  margin-bottom: 10px;
}
.our-class-header img {
  margin-bottom: 40px;
}
.our-class-info {
  margin: 0 auto;
  width: calc(100% / 2);
  display: flex;
  padding: 20px;
  margin-bottom: 60px;
}
.our-class-info h4 {
  font-size: 30px;
  color: #554e9e;
  margin-right: 40px;
}

.our-class-info p {
  font-size: 20px;
  line-height: 35px;
  color: grey;
}

/* cards */
.card-container {
  width: 100%;
  height: 600px;
}
.card {
  width: 100%;
  /* width: calc(100% / 2); */
}
.card-info {
  display: flex;
  background: #554e9e;
}
.card-image {
  width: calc(100% / 2);
  height: 150px;
}
.card-image img {
  width: 250px;
  height: 150px;
}
.card-image button {
  position: absolute;
}
</style>
