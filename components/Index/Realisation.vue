<template>
  <section class="rea">
    <div class="title_rea">
      <h3>Nos dernières réalisations</h3>
      <img src="~assets/img/svg/wave.svg" alt="" />
    </div>
    <div class="box_cards">
      <img src="~assets/img/png/img_1.jpg" alt="" />
      <img src="~assets/img/png/img_2.jpg" alt="" />
      <img src="~assets/img/png/img_3.jpg" alt="" />
      <img src="~assets/img/png/img_4.jpg" alt="" />
    </div>
    <div class="btn">
        <p>Nos réalisations</p>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {}
  },
}
</script>

<style scoped>
.rea {
  background: var(--background-gradient);
  padding-top: 30px;
}
.title_rea h3 {
  margin-bottom: 5px;
  padding: 0 26px;
  width: 300px;
}

.title_rea img {
  margin-bottom: 5px;
  padding: 0 26px;
}

.box_cards {
  position: relative;
  margin-top: 20px;
  margin-bottom: 50px;
}

.card_rea {
  text-align: center;
  margin: 0 20px;
  display: block;
  margin-bottom: 30px;
}

.box_cards img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.rec_left {
  position: absolute;
  background-color: var(--turquoise-light);
  top: -25px;
  left: 0px;
  z-index: -1;
  width: 100px;
  height: 100px;
}

.rec_right {
  position: absolute;
  background-color: var(--turquoise-light);
  bottom: -25px;
  right: 0px;
  z-index: -1;
  width: 100px;
  height: 100px;
}

.tns-carousel {
  margin-right: 20px !important;
}

.slide_tiny {
  display: flex;
  flex-flow: row nowrap;
  justify-content: center;
}

.tns-item {
  margin-left: 20px;
  width: 90% !important;
}

.slide_tiny .slidePrev {
  border: none;
  background-color: transparent;

  display: flex;
  justify-content: center;
  align-items: center;
  margin-right: 5px;
  margin-top: 10px;
  margin-bottom: 10px;
}

.slide_tiny .slideNext {
  border: none;
  background-color: transparent;
  display: flex;
  margin-top: 10px;
  margin-bottom: 10px;
  justify-content: center;
  align-items: center;
}

.slide_tiny .slidePrev img {
  transform: rotate(180deg);
}

.btn {
    text-align: center;
    margin: auto;
    margin-bottom: 50px;
}
</style>
