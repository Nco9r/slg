<template>
  <section class="news">
    <div class="block_news">
      <div class="block_left">
        <img src="~assets/img/png/mockupI.png" alt="" />
      </div>
      <div class="block_right">
        <div class="news_title">
          <p
            data-aos="fade-up"
            data-aos-offset="10"
            data-aos-delay="50"
            data-aos-duration="900"
          >
            Nouveau
          </p>
        </div>
        <div class="title_block">
          <h3
            data-aos="fade-up"
            data-aos-offset="10"
            data-aos-delay="50"
            data-aos-duration="900"
          >
            Automatisez votre piscine
          </h3>
        </div>
        <div class="content_block">
          <p
            data-aos="fade-up"
            data-aos-offset="10"
            data-aos-delay="70"
            data-aos-duration="900"
          >
            Avec le coffret connecté piscine tild et son application smartphone,
            faites le choix d’un bassin automatisé en toute simplicité !
          </p>
          <p
            data-aos="fade-up"
            data-aos-offset="10"
            data-aos-delay="90"
            data-aos-duration="900"
          >
            Entre filtration adaptée à la température de l’eau toute l’année,
            pilotage complet des projecteurs à tout moment sur le smartphone,
            tild devient votre assistant personnel rêvé.
          </p>
          <p
            data-aos="fade-up"
            data-aos-offset="10"
            data-aos-delay="110"
            data-aos-duration="900"
          >
            N'hesitez pas à nous contacter pour avoir de plus amples
            informations
          </p>
        </div>
        <nuxt-link to="/contact">
          <div
            class="btn"
            data-aos="fade-up"
            data-aos-offset="10"
            data-aos-delay="130"
            data-aos-duration="900"
          >
            En savoir plus
          </div>
        </nuxt-link>
      </div>
    </div>
  </section>
</template>

<script>
import aosMixin from '~/mixins/aos'
export default { mixins: [aosMixin] }
</script>

<style scoped>
.block_left {
  text-align: center;
  margin-top: 50px;
  margin-bottom: 30px;
}

.block_left img {
  width: 300px;
}

.block_right {
  padding: 20px 20px 20px 26px;
  background: var(--background-gradient-rotate);
}

.block_right .news_title {
  text-transform: uppercase;
  color: var(--baseline);
  font-size: 60px;
  font-weight: 900;
  margin-left: 10px;
}

.block_right .title_block h3 {
  margin-top: -30px;
  font-size: 22px;
}

.content_block {
  margin-top: 20px;
}

.content_block p {
  line-height: 28px;
  color: var(--bleu);
  margin-bottom: 20px;
}

.btn {
  width: 250px;
  text-align: center;
  margin-top: 40px;
  color: var(--bleu);
  font-weight: bold;
  margin-bottom: 50px;
}

@media screen and (min-width: 1024px) {
  .block_news {
    display: flex;
    justify-content: space-between;
    max-width: 900px;
    margin: 100px auto 30px auto;
  }

  .block_right .title_block h3 {
    font-size: 26px;
    margin-bottom: 45px;
  }

  .block_right .news_title {
    font-size: 80px;
  }

  .block_right {
    background: transparent;
    width: 55%;
  }

  .block_left {
    background: transparent;
    width: 43%;
    margin-top: 0px;
  }

  .block_left img {
    width: 100%;
  }
}

@media screen and (min-width: 1250px) {
  .block_news {
    display: flex;
    justify-content: space-between;
    max-width: 1200px;
    margin: 100px auto 30px auto;
  }

  .block_right .title_block h3 {
    font-size: 34px;
    margin-bottom: 45px;
  }

  .content_block p {
  line-height: 32px;
  color: var(--bleu);
  font-size: 18px;
  margin-bottom: 20px;
}

  .block_right .news_title {
    font-size: 80px;
  }

  .block_right {
    background: transparent;
    width: 55%;
  }

  .block_left {
    background: transparent;
    width: 43%;
    margin-top: 0px;
  }

  .block_left img {
    width: 100%;
  }
}

@media screen and (min-width: 1800px) {
  .block_news {
    display: flex;
    justify-content: space-between;
    max-width: 1700px;
    align-items: center;
    margin: 100px auto 30px auto;
  }

  .block_right .title_block h3 {
    font-size: 42px;
    margin-bottom: 45px;
    line-height: 56px;
  }

  .content_block p {
  line-height: 36px;
  color: var(--bleu);
  font-size: 20px;
  width: 600px;
  margin-bottom: 20px;
}



  .block_right .news_title {
    font-size: 140px;
  }

  .block_right {
    background: transparent;
    width: 45%;
  }

  .block_left {
    background: transparent;
    width: 40%;
    margin-top: 0px;
  }

  .block_left img {
    width: 100%;
  }
}
</style>
