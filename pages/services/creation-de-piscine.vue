<template>
<div>
    <div class="open">
      <img src="~assets/img/svg/wave_header.svg" alt="" />
    </div>
    <main>
        <hero-piscine/>
        <story/>
        <content-piscine/>
        <prestations-piscine/>
    </main>
</div>
  
</template>

<script>
import Story from '../../components/Index/Story.vue'
import ContentPiscine from '../../components/Realisations/Services/ContentPiscine.vue'
import HeroPiscine from '../../components/Realisations/Services/HeroPiscine.vue'
import PrestationsPiscine from '../../components/Realisations/Services/PrestationsPiscine.vue'
export default {
  components: { HeroPiscine, Story, ContentPiscine, PrestationsPiscine },

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

</style>