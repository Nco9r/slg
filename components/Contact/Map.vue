<template>
  <section class="map">
    <div class="title_map">
      <h3>Nous trouver</h3>
      <p>95 avenue du Maréchal de Lattre de Tassigny <br> 33610, Cestas</p>
      <p>Lun - Ven : 9h - 18h</p>
      <img src="~assets/img/svg/wave.svg" alt="" />
    </div>
    <a
      href="https://www.google.com/maps/place/Slgrealisation/@44.7567425,-0.7371421,15z/data=!4m5!3m4!1s0x0:0xa0c815c1940cf19a!8m2!3d44.7567425!4d-0.7371421"
      target="_blank"
    >
      <div class="img_map">
        <img src="~assets/img/svg/points.svg" alt="" />

        <img src="~assets/img/png/map.jpg" alt="" />

        <div class="rec_right"></div>
      </div>
    </a>
  </section>
</template>

<script>
export default {}
</script>

<style scoped>
.map {
  margin-top: 30px;
  padding: 20px 26px 20px 26px;
  margin-bottom: 50px;
  overflow: hidden;
}

.title_map p {
    color: var(--bleu);
}

.img_map {
  margin-top: 50px;
  position: relative;
}

.img_map img:nth-child(2) {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.img_map img:nth-child(1) {
  position: absolute;
  left: -20px;
  width: 200px;
  z-index: -1;
  margin-top: -20px;
}

.rec_right {
  position: absolute;
  right: -50px;
  background-color: var(--turquoise);
  height: 100px;
  width: 100px;
  z-index: -1;
  bottom: -20px;
}

@media screen and (min-width: 1024px) {
  .map {
    max-width: 800px;
    margin: 50px auto 150px auto;
  }
  .img_map img:nth-child(2) {
    width: 100%;
    height: 400px;
    object-fit: cover;
  }


  .rec_right {
    position: absolute;
    right: -50px;
    background-color: var(--turquoise);
    height: 300px;
    width: 300px;
    z-index: -1;
    bottom: -20px;
  }

  .img_map img:nth-child(1) {
    position: absolute;
    left: -20px;
    width: 300px;
    z-index: -1;
    margin-top: -20px;
  }

  .title_map {
      text-align: center;
      margin-bottom: 50px;
  }

  .title_map h3 {
      font-size: 34px;
      margin-bottom: 10px;
  }
}
</style>
