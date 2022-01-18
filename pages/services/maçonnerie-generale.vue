<template>
  <div>
    <div class="open">
      <img src="~assets/img/svg/wave_header.svg" alt="" />
    </div>
    <main>
    <hero-macon/>
      <div class="breadcrum">
          <p>Accueil - Services - <span class="turquoise">Maçonnerie Générale</span></p>
      </div>
      <story />
      <macon-content/>
      <visit />
        <macon-other/>
      <cta/>
    </main>
  </div>
</template>

<script>
import Cta from '../../components/Index/Cta.vue'
import News from '../../components/Index/News.vue'
import Story from '../../components/Index/Story.vue'
import Visit from '../../components/Index/Visit.vue'
import HeroMacon from '../../components/Realisations/Services/Maconnerie/HeroMacon.vue'




import MaconContent from '../../components/Realisations/Services/Maconnerie/MaconContent.vue'
import MaconOther from '../../components/Realisations/Services/Maconnerie/MaconOther.vue'

export default {
  components: {

    Story,


    News,
    Visit,
    Cta,

    MaconContent,
    HeroMacon,
    MaconOther,
  },
   
}
</script>

<style scoped>
.open {
  position: fixed;
  inset: 0;
  z-index: 1000;
  background-color: var(--turquoise);
  animation: bck 3s ease-in-out;
  animation-fill-mode: forwards;
}

.turquoise {
    font-weight: bold;
}

.open img {
  margin-top: -80px;
  opacity: 0;
  animation: appear 0.6s ease-in-out;
  animation-fill-mode: forwards;
  animation-delay: 1.3s;
}

@keyframes bck {
  0% {
    background-color: var(--bleu);
    transform: translateY(0);
  }

  60% {
    background-color: var(--turquoise);
    transform: translateY(0);
  }
  100% {
    transform: translateY(115%);
  }
}

@keyframes appear {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 1;
  }
}

.breadcrum {
    padding: 30px 26px 0px 26px;
    margin-bottom: -70px;
}

.breadcrum p {
    font-size: 12px;
    color: var(--bleu);
}


@media screen and (min-width: 1250px) {
  .breadcrum {
    max-width: 1200px;
    margin: auto;
  }

  .breadcrum p {
    font-size: 16px;
    color: var(--bleu);
}
}

@media screen and (min-width: 1800px) {
  .breadcrum {
    max-width: 1700px;
    margin: auto;
   
  }

  .breadcrum p {
    font-size: 16px;
    color: var(--bleu);
}
}
</style>
