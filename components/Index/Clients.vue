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
                la piscine de qualité !
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
                <p>P</p>
              </div>
              <div class="logo">
                <img src="~assets/img/svg/gb.svg" alt="" />
              </div>
            </div>
            <div class="content_card_client">
              <p>
                Extrêmement satisfait de la construction d'une piscine par cette
                entreprise : conseil, compétence, réalisation soignée , le tout
                au top et en respectant le calendrier fixé ! Sans oublier la
                disponibilité et la gentillesse!!! Je la recommande sans aucune
                hésitation
              </p>
            </div>
            <div class="client">
              <p>Dubern Eric -</p>
              <p>Création piscine</p>
            </div>
          </div>
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
                Une entreprise très sérieuse avec des personnes à l'écoute de
                vos projets. En résulte, un travail de grande qualité. Toujours
                à l'heure et un chantier très propre. Nous sommes très
                satisfaits et recommandons vivement Slg.realisation !!
              </p>
            </div>
            <div class="client">
              <p>Audrey Issury -</p>
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
                Je recommande vivement !
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
    <div class="btn center">
      <a href="https://www.google.com/search?q=slg+realisation&rlz=1C5CHFA_enFR969FR969&oq=slg+re&aqs=chrome.0.69i59j46i39i175i199j69i57j0i512l2j69i60j69i61l2.1061j0j7&sourceid=chrome&ie=UTF-8#lrd=0xd54dd3bc92586dd:0xa0c815c1940cf19a,1,,," target="_blank" rel="noopener noreferrer">
      <p>Voir nos avis</p>
      </a>
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
        nav: true,
        autoplay: true,
        navPosition: 'bottom',
        autoplayTimeout: 3500,
        speed: 500,
        autoplayButtonOutput: false,
        gutter: 0,
        preventScrollOnTouch: 'auto',
        controls: true,
        prevButton: '#prev',
        nextButton: '#next',
        responsive: {
           1024: {
            items: 2, 
          },
           1180: {
            items: 3, 
          },
          1500: {
            items: 4, 
          }
        }
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

<style>
.clients {
  padding: 0 0px;
  margin-bottom: 50px;
}
.title_client {
  text-align: center;
}

.box_cards_clients {
  margin-top: 20px;
  position: relative;
  margin-bottom: 30px;
}

.tns-nav {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100px;
  margin: auto;
}

.tns-nav button {
  border: 1px solid var(--turquoise);
  background-color: transparent;
  margin-right: 10px;
  height: 14px;
  width: 14px;
  border-radius: 50%;
}

tns-nav-active {
  background-color: var(--bleu) !important;
}

.card_client {
  background-color: var(--white);
 box-shadow: rgb(0 0 0 / 10%) 0px 10px 30px;
  height: 350px;
  border-radius: 0 25px 0 25px;
  width: 200px;
  padding: 30px 20px;
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
  height: 133px;
  color: var(--bleu);
  text-overflow: ellipsis;

  overflow: hidden;
}

.client {
  display: flex;
  margin-top: 30px;
  margin-bottom: 20px;
}

.tns-item {
  margin-right: 15px;
  margin-left: 15px;
  margin-bottom: 20px;
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
  text-transform: uppercase;
  font-size: 12px;
}

.center {
  margin: auto;
  margin-top: 20px;
  margin-bottom: 20px;
}

@media screen and (min-width: 1024px) {
  .title_client h3 {
    font-size: 26px;
  }
}

@media screen and (min-width: 1250px) {
  .title_client h3 {
    font-size: 34px;
  }

  .title_client {
    margin-bottom: 50px;
  }
}
</style>
