<template>
  <div>
    <div class="open">
      <img src="~assets/img/svg/wave_header.svg" alt="" />
    </div>
    <main>
      <hero />
      <story />
      <baseline />
      <prestations />
      <visit />
      <news />
      <realisation />
      <partenaires />
      <clients />
      <maaf />
      <cta />
    </main>
  </div>
</template>

<script>
import Baseline from '../components/Index/Baseline.vue'
import Clients from '../components/Index/Clients.vue'
import Cta from '../components/Index/Cta.vue'
import Hero from '../components/Index/Hero.vue'
import Maaf from '../components/Index/Maaf.vue'
import News from '../components/Index/News.vue'
import Partenaires from '../components/Index/Partenaires.vue'
import Prestations from '../components/Index/Prestations.vue'
import Realisation from '../components/Index/Realisation.vue'
import Story from '../components/Index/Story.vue'
import Visit from '../components/Index/Visit.vue'

export default {
  components: {
    Hero,
    Story,
    Baseline,
    Prestations,
    Visit,
    News,
    Realisation,
    Partenaires,
    Maaf,
    Cta,
    Clients,
  },
}
</script>

<style>
.open {
  position: fixed;
  inset: 0;
  z-index: 1000;
  background-color: var(--turquoise);
  animation: bck 3s ease-in-out;
  animation-fill-mode: forwards;
}

.open img {
  margin-top: -80px;
  opacity: 0;
  animation: appear .6s ease-in-out;
  animation-fill-mode: forwards;
  animation-delay: 1.3s;
   
 
}

@keyframes bck {
  0% {
    background-color: var(--bleu);
    
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
</style>
