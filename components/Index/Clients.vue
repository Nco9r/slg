<template>
  <section class="clients">
    <div class="title_client">
      <h3>Les avis de nos clients</h3>
      <img src="~assets/img/svg/wave.svg" alt="" />
    </div>
    <div class="box_cards_clients">
      <no-ssr>
        <vue-tiny-slider v-bind="tinySliderOptions" ref="tinySlider">
          <div class="card_client">
            <div class="entete">
              <div class="name">
                <p>P</p>
              </div>
              <div class="logo">
                <img src="~assets/img/svg/gb.svg" alt="" />
              </div>
            </div>
            <div class="content_card_client">
              <p>
                Travail en famille rapide et de grande qualité Intervenants très
                disponibles à l'écoute et de bon conseil Le choix du matériel de
                la piscine de qualité
              </p>
            </div>
            <div class="client">
              <p>Pascal Barbeau -</p>
              <p>Création piscine</p>
            </div>
          </div>
          <div class="card_client">
            <div class="entete">
              <div class="name">
                <p>J</p>
              </div>
              <div class="logo">
                <img src="~assets/img/svg/gb.svg" alt="" />
              </div>
            </div>
            <div class="content_card_client">
              <p>
                Une entreprise effectuant un travail remarquable. Très sérieux.
                Je recommande vivement
              </p>
            </div>
            <div class="client">
              <p>Julie Triscos -</p>
              <p>Création piscine</p>
            </div>
          </div>
          <div class="card_client">
            <div class="entete">
              <div class="name">
                <p>E</p>
              </div>
              <div class="logo">
                <img src="~assets/img/svg/gb.svg" alt="" />
              </div>
            </div>
            <div class="content_card_client">
              <p>
                Maçon consciencieux et appliqué, travail de qualité, réactivité
                et delais respectés ! Je recommande a tous ceux qui ont besoin
                d'une personne qualifié dans ce domaine d'activité !
              </p>
            </div>
            <div class="client">
              <p>Eliott Cassaignau -</p>
              <p>Création piscine</p>
            </div>
          </div>
        </vue-tiny-slider>
      </no-ssr>
    </div>
    <div class="btn">
        <p>Voir nos avis</p>
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

         autoplayTimeout: 3500,
        speed: 500,
        autoplayButtonOutput: false,
        gutter: 0,
        preventScrollOnTouch: 'auto',
        controls: true,
        prevButton: '#prev',
        nextButton: '#next',
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
.clients {
  padding: 0 0px;
  margin-bottom: 50px;

}
.title_client {
  text-align: center;
}

.box_cards_clients {
  margin-top: 50px;
  position: relative;
  margin-bottom: 30px;
}

.tns-nav button {
  background-color: var(--turquoise) !important;
  color: var(--bleu);
}



.card_client {
   background-color: var(--white);
box-shadow: 0px 0px 15px 0px rgba(0,0,0,0.1);
  height: 350px;
  width: 200px;
  padding: 40px 20px;
  display: block;
}

.entete {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.name {
  background-color: slateblue;
  width: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50px;
  border-radius: 50%;
  color: var(--white);
  font-weight: bold;
}


.content_card_client p {
  line-height: 28px;
  margin-top: 20px;
  height: 130px;
  color: var(--bleu);
}

.client {
  display: flex;
  margin-top: 30px;
  margin-bottom: 20px;
}


.tns-item {
  margin-right: 20px;
margin-left: 20px;
  display: block;
}

.tns-carousel {
  display: flex;
  flex-flow: row nowrap;
  margin-top: 15px;
  margin-bottom: 15px;
  justify-content: center;
}

.client p {
  font-weight: bold;
  margin-right: 5px;
  color: var(--bleu);
}

.btn {
    margin: auto;
    margin-top: 20px;
    margin-bottom: 20px;
}
</style>
