<template>
  <section class="prestations">
    <div class="title_prestations">
      <h3>Nos différentes prestations</h3>
      <img src="~assets/img/svg/wave.svg" alt="" />
    </div>
    <div class="box_cards">
      <div class="rec_left"></div>
      <div class="rec_right"></div>
      <no-ssr>
        <vue-tiny-slider v-bind="tinySliderOptions" ref="tinySlider">
          <div class="card">
            <div class="img_card">
              <img src="~assets/img/svg/icon_pis.svg" alt="" />
            </div>
            <div class="title_card">
              <h4>Création de piscine</h4>
            </div>
            <div class="content_card">
              <p>
                Réalisation de piscine traditionnelle ou en block polystyrène.
                Toute taille fond incliné ou droit.
              </p>
            </div>
            <div class="btn_card">
              <nuxt-link to="/services/creation-de-piscine">
              <p>En savoir plus</p>
              </nuxt-link>
            </div>
          </div>
          <div class="card">
            <div class="img_card second">
              <img src="~assets/img/svg/icon_mac.svg" alt="" />
            </div>
            <div class="title_card">
              <h4>Maçonnerie generale</h4>
            </div>
            <div class="content_card">
              <p>
                Réalisation de maison ou extension, aménagement extérieur, pool
                house, terrasse, murette.
              </p>
            </div>
            <div class="btn_card">
              <p>En savoir plus</p>
            </div>
          </div>
          <div class="card">
            <div class="img_card">
              <img src="~assets/img/svg/icon_ter.svg" alt="" />
            </div>
            <div class="title_card">
              <h4>Terrassement</h4>
            </div>
            <div class="content_card">
              <p>
                Chemin d’accès, passage de réseau divers, pose de casier
                drainant, terrain de pétanque.
              </p>
            </div>
            <div class="btn_card">
              <p>En savoir plus</p>
            </div>
          </div>
        </vue-tiny-slider>
      </no-ssr>
    </div>
   
    <div class="slide_tiny">
      <button class="slidePrev" id="prev">
        <img src="@/assets/img/svg/arrow.svg" alt="" />
      </button>
      <button class="slideNext" id="next">
        <img src="@/assets/img/svg/arrow.svg" alt="" />
      </button>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      tinySliderOptions: {
        mouseDrag: true,
        loop: false,
        items: 1,
        nav: false,
        autoplayButtonOutput: false,
        gutter: 0,
        preventScrollOnTouch: 'auto',
        controls: true,
        prevButton: '#prev',
        nextButton: '#next',
        responsive: {
          1014: {
            items: 3,
            loop: false,
            prevButton: '#prev',
            nextButton: '#next',
          },
        },
      },
    }
  },
  head() {
    return {
      link: [
        {
          rel: 'stylesheet',
          href: 'https://cdnjs.cloudflare.com/ajax/libs/tiny-slider/2.9.1/tiny-slider.css',
        },
      ],
    }
  },
}
</script>

<style scoped>
.title_prestations {
  text-align: center;
}

.title_prestations h3 {
  margin-bottom: 5px;
  padding: 0 20px;
}

.box_cards {
  position: relative;
  margin-top: 70px;

  margin-bottom: 50px;
}

a {
  text-decoration: none;
  color: var(--turquoise);
}

.card {
  background-color: var(--white);
  text-align: center;
  height: 330px;

  padding: 40px 20px;

  display: block;
}
.tns-controls {
  display: none;
}

.tns-nav {
  display: none !important;
}
.img_card img {
  width: 70px;
  height: 50px;
}

.slide_tiny {
  display: block;
}

.tns-item {
  margin-right: 20px;
margin-left: 20px;
  display: block;
}

.tns-carousel {
  display: flex;
  flex-flow: row nowrap;
  justify-content: center;
}

.second img {
  width: 50px;
}

.title_card {
  margin-top: 20px;
  color: var(--bleu);
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
}

.content_card {
  color: var(--bleu);
  line-height: 28px;
  margin-bottom: 20px;
  height: 90px;
}

.btn_card {
  font-weight: bold;
  color: var(--turquoise);
  font-size: 14px;
}

.rec_left {
  position: absolute;
  background-color: var(--turquoise);
  top: -10px;
  left: 0px;
  z-index: -1;
  width: 100px;
  height: 100px;
}

.rec_right {
  position: absolute;
  background-color: var(--turquoise);
  bottom: 10px;
  right: 0px;
  z-index: -1;
  width: 100px;
  height: 100px;
}


.slide_tiny {
  display: flex;
  flex-flow: row nowrap;
  justify-content: center;
  margin-top: -50px;
  margin-bottom: 20px;
}

/* .tns-item {
  padding: 40px 20px;
  margin-left: 25px;
  margin-right: 15px;
  text-align: center;
  width: 325px!important;
} */


.slide_tiny .slidePrev {
  border: none;
  background-color: transparent;

  display: flex;
  justify-content: center;
  align-items: center;
  margin-right: 5px;
  margin-top: 5px;
  margin-bottom: 5px;
}

.slide_tiny .slideNext {
  border: none;
  background-color: transparent;
  display: flex;
  margin-top: 5px;
  margin-bottom: 5px;
  justify-content: center;
  align-items: center;
}

.slide_tiny .slidePrev img {
  transform: rotate(180deg);
}

@media screen and (min-width: 1024px) {


  .title_prestations h3 {
    font-size: 34px;
    line-height: 46px;
  }
  .tns-item {
    padding: 40px 20px;
    margin-left: 20px;
    width: 420px !important;
  }

  .tns-item:nth-child(1) {
    padding: 40px 20px;
    margin-left: 70px;
    width: 420px !important;

  }

  .rec_left {
    display: none;
  }

  .rec_right {
    display: none;
  }

  .slide_tiny {
    display: flex;
    margin-top: 0px;

    z-index: 9;
    flex-flow: row nowrap;
    justify-content: flex-start;
  }
}
</style>
