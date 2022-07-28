<template>
  <section>
    <div class="ourclass-header">
      <h1>Our Classes</h1>
      <h4>Our preschool program has four dedicated class</h4>
      <img src="../assets/images/header_divider.png" alt="header divider" />
      <div class="ourclass-info">
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
            <p>Class name</p>
            <p>{{ card.age }}</p>
            <p>Month olds</p>
            <p>{{ card.size }}</p>
            <p>Class size</p>
            <div class="card-image">
              <img :src="card.images" alt="" />
              <a href="#">READ MORE</a>
            </div>
          </div>
        </div>
      </div>

      <div class="ourclass-footer">
        <div class="ourclass-right-footer">
          <h4>
            We have been educating children for over fifteen years. Our goal is
            to create a place that engages each child
          </h4>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui,
            reiciendis non unde aperiam nobis quam exercitationem accusamus
            quidem quod laboriosam eligendi. Neque atque magni inventore odit
            natus repudiandae libero! Laboriosam!
          </p>
          <ul>
            <li>Comprehensive reporting on individual achievment</li>
            <li>Comprehensive reporting on individual achievment</li>
            <li>Comprehensive reporting on individual achievment</li>
            <li>Comprehensive reporting on individual achievment</li>
            <li>Comprehensive reporting on individual achievment</li>
            <li>Comprehensive reporting on individual achievment</li>
          </ul>
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
.ourclass-header {
  width: 100%;
  height: auto;
  text-align: center;
}
.ourclass-header h1 {
  font-size: 50px;
  color: #554e9e;
  padding: 10px;
}
.ourclass-header > h4 {
  color: grey;
  padding: 10px;
  font-size: 18px;
  margin-bottom: 10px;
}
.ourclass-header img {
  margin-bottom: 40px;
}
.ourclass-info {
  margin: 0 auto;
  width: calc(100% / 2);
  display: flex;
  padding: 20px;
  margin-bottom: 60px;
}
.ourclass-info h4 {
  font-size: 30px;
  color: #554e9e;
  margin-right: 40px;
}

.ourclass-info p {
  font-size: 20px;
  line-height: 35px;
  color: grey;
}

/* cards */
.card-container {
  max-width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  margin-bottom: 60px;
}
.card {
  margin: 10px;
}
.card-info {
  display: flex;
  width: 100%;
  height: auto;
  background: #554e9e;
}
.card-image {
  display: flex;
  justify-content: flex-end;
  width: 100%;
  height: 150px;
}
.card-image img {
  width: 250px;
  height: 150px;
}
.card-image a {
  position: absolute;
  border: none;
  padding: 10px;
  background-color: #fe6601;
  text-decoration: none;
  color: white;
  margin-top: 112px;
}
/* footer-section  */
.ourclass-footer {
  background-color: #e8e6e7;
  width: 100%;
  height: auto;
}
.ourclass-right-footer {
  width: calc(80% / 2);
  text-align: left;
  overflow: hidden;
}
</style>
