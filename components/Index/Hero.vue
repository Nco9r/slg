<template>
  <section class="hero_banner">
    <div class="hero_img">
      <no-ssr>
        <vue-tiny-slider v-bind="tinySliderOptions" ref="tinySlider">
          <img src="~assets/img/png/home_img.jpg" alt="" />
          
          <img src="~assets/img/png/img_2.jpg" alt="" />

        </vue-tiny-slider>
      </no-ssr>
       <div class="slide_tiny">
      <button class="slidePrev" id="prev">
        <img src="@/assets/img/svg/arrow.svg" alt="" />
      </button>
      <button class="slideNext" id="next">
        <img src="@/assets/img/svg/arrow.svg" alt="" />
      </button>
    </div>
    </div>
    <div class="hero_content">
      <div class="title_hero">
        <h1>
          Maçonnerie, Terrassement, <span class="turquoise">Pisciniste</span> à
          Cestas. (33)
        </h1>
        <img src="~assets/img/svg/wave.svg" alt="" />
      </div>
      <div class="btn">
        <nuxt-link to="/contact">
          <p>Devis Gratuit</p>
        </nuxt-link>
      </div>
    </div>
    <div class="mouse">
      <img src="~assets/img/svg/mouse.svg" alt="" />
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
        tinySliderOptions: {
        mouseDrag: true,
        loop: true,
        items: 1,
        nav: false,
        autoplay: true,
        navPosition: 'bottom',
        autoplayTimeout: 3500,
        speed: 500,
        autoplayButtonOutput: false,
        gutter: 0,
        mode: 'carousel',
        preventScrollOnTouch: 'auto',
        controls: true,
        prevButton: '#prev',
        nextButton: '#next',
      },
    }
  }
}

</script>

<style scoped>
/* VARIABLES */

.turquoise {
  color: var(--turquoise);
}

/* PAGE */

.hero_banner {
  position: relative;
  margin-top: 70px;
}

.hero_img {
  position: relative;
}

.hero_img img {
  width: 100%;
  object-fit: cover;
  height: 90%;
}

.hero_content {
  background-color: var(--bleu);
  margin-top: -20px;
  width: 100%;
  z-index: 11;
  height: 510px;
  background-image: url('~assets/img/svg/carre.svg');
  background-size: 135%;
  padding: 10px 45px 10px 35px;
}

.title_hero h1 {
  margin-top: 30px;
  font-size: 32px;
  line-height: 46px;
  font-weight: 900;
  margin-bottom: 15px;
  color: var(--white);
}

.tns-item {
  margin-right: 0px;
  margin-left: 0px;
  margin-bottom: 0px;
  display: block;
}

.tns-gallery {
  display: flex;
  flex-flow: row nowrap;
  margin-top: 15px;
  margin-bottom: 15px;
  justify-content: center;
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
  position: absolute;
  top: 50%;
  left: 10px;
}

.slide_tiny .slideNext {
 border: none;
  background-color: transparent;
  position: absolute;
  top: 50%;
  right: 10px;
}

.slide_tiny .slidePrev img {
  transform: rotate(180deg);
  width: 25px;
}
.slide_tiny .slideNext img {

  width: 25px;
}

.btn {
  margin-top: 30px;
  text-align: center;
  font-weight: 700;
  width: 250px;
  color: var(--bleu);
}

.mouse {
  position: absolute;
  bottom: 80px;
  left: 50%;
  animation: scroll 1.2s infinite ease-in-out;
}

@keyframes scroll {
  0% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(20px);
  }
  100% {
    transform: translateY(0px);
  }
}

@media screen and (min-width: 1024px) {
  .hero_img img {
    width: 84.2%;

    object-fit: cover;
    height: 90vh;
    margin-right: -90px;
  }

  .btn  {
    margin: 0;
  }

  .hero_banner {
    margin-top: 100px;
  }

  .hero_content {
    position: absolute;
    width: 500px;
    height: 500px;

    right: 0;
    padding: 20px 30px 40px 50px;
    bottom: -50px;
  }

  .title_hero h1 {
    margin-top: 30px;
    font-size: 34px;
    line-height: 42px;
    width: 400px;
    font-weight: 900;
    margin-bottom: 15px;
    color: var(--white);
  }
  .mouse {
    bottom: 130px;

    left: 95%;
  }
}
</style>
