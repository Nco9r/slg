<template>
  <section class="hero_banner">
    <div class="hero_img">
      <img src="~assets/img/png/contact_img.jpg" alt="" />
    </div>
    <div class="hero_content">
      <div class="title_hero">
        <h1>
          Contactez nous pour tous <span class="turquoise">renseignements.</span>
        </h1>
        <img src="~assets/img/svg/wave.svg" alt="" />
      </div>
      <div class="items_infos">
          <div class="item">
              <img src="~assets/img/svg/mail.svg" alt="">
              <p>contact@slgrealisation.fr</p>
          </div>
          <div class="item">
              <img src="~assets/img/svg/phone.svg" alt="">
              <p>06 83 97 65 90</p>
          </div>
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

section {
    overflow: hidden;
}

.hero_banner {
  overflow-x: hidden;

  position: relative;
  margin-top: 70px;
}

.hero_img img {
  width: 100%;
  object-fit: cover;
  height: 90%;
}

.hero_content {
  background-color: var(--bleu);
  margin-top: -10px;
  width: 100%;
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

.items_infos {
    margin-top: 30px;
    display: flex;
    flex-flow: column;
    justify-content: center;
}

.item {
    display: flex;
    margin-bottom: 10px;
}

.item:nth-child(2) {
    display: flex;margin-left: 3px;
    margin-bottom: 10px;
}

.item p {
    margin-left: 10px;
    color: var(--white);
    font-weight: bold;
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
    width: 300px;
    font-weight: 900;
    margin-bottom: 15px;
    color: var(--white);
  }
  .mouse {
    bottom: 70px;

    left: 90%;
  }

}
</style>
