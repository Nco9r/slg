<template>
  <section class="hero_banner">
    <div class="hero_img">
      <img src="~assets/img/png/rea_img.jpg" alt="" />
    </div>
    <div class="hero_content">
      <div class="title_hero">
        <h1>
          Découvrez nos <span class="turquoise">réalisations</span> sur Bordeaux et sa Région.
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
export default {}
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
  height: 510px;
  background-image: url('~assets/img/svg/carre.svg');
  background-size: 135%;
  padding: 10px 45px 10px 35px;
  border-radius: 0 0px 0 25px;
}

.title_hero {
  opacity: 0;
  animation: appear 0.5s ease-in-out;
  animation-fill-mode: forwards;
  animation-delay: 2.4s;
}

.title_hero h1 {
  margin-top: 30px;
  font-size: 32px;
  line-height: 46px;
  font-weight: 900;
  margin-bottom: 15px;
  color: var(--white);
}

@keyframes appear {
  from {
    transform: translateY(30px);
    opacity: 0;
  }
  to {
    transform: translateY(0px);
    opacity: 1;
  }
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

.slide_tiny_hero {
  display: block;
}

.slide_tiny_hero .slidePrev_hero {
  border: none;
  background-color: transparent;
  position: absolute;
  top: 50%;
  left: 10px;
}

.slide_tiny_hero .slideNext_hero {
  border: none;
  background-color: transparent;
  position: absolute;
  top: 50%;
  right: 10px;
}

.slide_tiny_hero .slidePrev_hero img {
  transform: rotate(180deg);
  width: 25px !important;
  height: 25px;
}
.slide_tiny_hero .slideNext_hero img {
  width: 25px;
  height: 25px;
}

.btn {
  margin-top: 30px;
  text-align: center;
  font-weight: 700;
  width: 250px;
  opacity: 0;
  animation: appear 0.5s ease-in-out;
  animation-fill-mode: forwards;
  animation-delay: 2.4s;
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
    width: 100%;

    object-fit: cover;
    height: 620px;
  }

  .slide_tiny_hero .slidePrev_hero {
    border: none;
    background-color: transparent;
    position: absolute;
    top: 88%;
    left: 50px;
  }

  .slide_tiny_hero .slideNext_hero {
    border: none;
    background-color: transparent;
    position: absolute;
    top: 88%;
    left: 110px;
  }

  .slide_tiny_hero .slidePrev_hero img {
    transform: rotate(180deg);
    width: 35px !important;
    height: 35px;
  }
  .slide_tiny_hero .slideNext_hero img {
    width: 35px;
    height: 35px;
  }

  .btn  {
    margin: 0;
  }

  .hero_banner {
    margin-top: 90px;
  }

  .hero_content {
    position: absolute;
    width: 500px;
    height: 500px;

    right: 0;
    padding: 20px 30px 40px 50px;
    bottom: -100px;
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

@media screen and (min-width: 1250px) {
  .hero_img img {
    width: 100%;

    object-fit: cover;
    height: 820px;
  }

  .slide_tiny_hero .slidePrev_hero {
    border: none;
    background-color: transparent;
    position: absolute;
    top: 88%;
    left: 50px;
  }

  .slide_tiny_hero .slideNext_hero {
    border: none;
    background-color: transparent;
    position: absolute;
    top: 88%;
    left: 110px;
  }

  .slide_tiny_hero .slidePrev_hero img {
    transform: rotate(180deg);
    width: 35px !important;
    height: 35px;
  }
  .slide_tiny_hero .slideNext_hero img {
    width: 35px;
    height: 35px;
  }

  .btn  {
    margin-top: 90px;
  }

  .hero_banner {
    margin-top: 90px;
  }

  .hero_content {
    position: absolute;
    width: 600px;
    height: 600px;
    z-index: 2;
    right: 0;
    padding: 20px 30px 40px 50px;
    bottom: -100px;
  }

  .title_hero h1 {
    margin-top: 30px;
    font-size: 42px;
    line-height: 62px;
    width: 400px;
    font-weight: 900;
    margin-bottom: 15px;
    color: var(--white);
  }
  .mouse {
    top: 88%;

    left: 50%;
  }
}

@media screen and (min-width: 1800px) {
 .hero_img img {
    width: 100%;

    object-fit: cover;
    height: 920px;
  }

  .hero_content {
  
    width: 700px;
    height: 700px;
  }

  .title_hero h1 {
    margin-top: 30px;
    font-size: 52px;
    line-height: 72px;
    width: 400px;
    font-weight: 900;
    margin-bottom: 15px;
    color: var(--white);
  }
}
</style>
