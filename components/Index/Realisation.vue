<template>
  <div class="box_rea">
    <section class="rea">
      <div class="title_rea">
        <h3>Nos dernières réalisations</h3>
        <img src="~assets/img/svg/wave.svg" alt="" />
      </div>
      <div class="box_cards">
        <div class="box_point">
          <img src="~assets/img/svg/points.svg" alt="" />
        </div>
        <img src="~assets/img/png/img_1.jpg" alt="" />
        <img src="~assets/img/png/img_2.jpg" alt="" />
        <img src="~assets/img/png/img_3.jpg" alt="" />
        <img src="~assets/img/png/img_4.jpg" alt="" />
        <div class="box_rec"></div>
      </div>
      <nuxt-link to="/realisations">
        <div class="btn">Nos réalisations</div>
      </nuxt-link>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
}
</script>

<style scoped>
.box_rea {
  background: var(--background-gradient);
  padding: 30px 15px 0px 15px;
}
.title_rea h3 {
  margin-bottom: 5px;
  padding: 0 16px;
  width: 300px;
}

.title_rea img {
  margin-bottom: 5px;
  padding: 0 16px;
}

.box_cards {
  position: relative;
  margin-top: 20px;
  margin-right: 10px;
  margin-left: 10px;
  z-index: 2;
  margin-bottom: 50px;
}

.card_rea {
  text-align: center;
  margin: 0 26px;
  display: block;
  margin-bottom: 40px;
}

.box_cards img {
  width: 100%;
  margin-bottom: 20px;
  z-index: 2;
  height: 100%;
  border-radius: 0 25px 0 25px;
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

.box_point {
  display: none;
}

@media screen and (min-width: 1024px) {
  .rea {
    max-width: 900px;
    margin: 30px auto;
  }

  .title_rea {
    margin-bottom: 60px;
  }

  .title_rea h3 {
    font-size: 26px;
    width: 600px;
  }

  .box_cards {
    display: flex;
    position: relative;
    flex-flow: row wrap;
    align-items: center;
    justify-content: space-between;
  }

  .box_point {
    position: absolute;
    display: flex;
    top: -30px;
    left: -30px;
  }

  .box_rec {
    position: absolute;
    display: flex;
    width: 300px;
    height: 300px;
    background: var(--turquoise);
    bottom: 0px;
    right: -30px;
  }

  .box_point img {
    width: 350px !important;
  }

  .box_cards img {
    width: 48%;
    margin-bottom: 30px;
    cursor: pointer;
    transition: all 0.3s;
  }

  .box_cards img:hover {
    transform: scale(1.03);
    opacity: 0.8;
  }
}

@media screen and (min-width: 1250px) {
  .rea {
    max-width: 1200px;
    margin: 70px auto;
  }

    .title_rea h3 {
    font-size: 34px;
    width: 600px;
  }

    .box_cards img {
    width: 48%;
    margin-bottom: 30px;
    height: 300px;
    cursor: pointer;
    transition: all 0.3s;
  }
}

@media screen and (min-width: 1800px) {
  .rea {
    max-width: 1700px;
    margin: 70px auto;
  }

    .title_rea h3 {
    font-size: 42px;
    width: 600px;
  }

    .box_cards img {
    width: 48%;
    margin-bottom: 60px;
    height: 400px;
    cursor: pointer;
    transition: all 0.3s;
  }

    .box_point {
    position: absolute;
    display: flex;
    top: -50px;
    left: -50px;
  }

  .box_rec {
    position: absolute;
    display: flex;
    width: 600px;
    height: 300px;
    background: var(--turquoise);
    bottom: 0px;
    right: -80px;
  }
}

</style>
