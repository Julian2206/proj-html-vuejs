<template>
  <section>
    <div>
      <div class="ourstaff-header">
        <h1>Meet Our Staff</h1>
        <h4>With education and experience in early childhood care</h4>
        <img src="../assets/images/header_divider.png" alt="header divider" />
        <div class="ourstaff-info">
          <h4>
            Our staff consists of three teachers and one assistant with
            experience in early childhood care.
          </h4>
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolorem,
            sit qui. Omnis obcaecati illo at reiciendis delectus culpa nulla
            quod quae, adipisci aspernatur enim sapiente aperiam hic! Optio,
            iste expedita.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style>
.ourstaff-header {
  width: 100%;
  height: auto;
  text-align: center;
}
.ourstaff-header h1 {
  font-size: 50px;
  color: #554e9e;
  padding: 10px;
}
.ourstaff-header > h4 {
  color: grey;
  padding: 10px;
  font-size: 18px;
  margin-bottom: 10px;
}
.ourstaff-header > img {
  margin-bottom: 40px;
}
.ourstaff-info {
  margin: 0 auto;
  width: calc(100% / 2);
  display: flex;
  padding: 20px;
  margin-bottom: 60px;
}
.ourstaff-info h4 {
  font-size: 30px;
  color: #554e9e;
  margin-right: 40px;
}
.ourstaff-info > p {
  font-size: 20px;
  line-height: 35px;
  color: grey;
}
</style>
