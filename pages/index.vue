<template>
  <main>
    <hero/>
    <story/>
    <baseline/>
    <prestations/>
    <visit/>
    <news/>
    <realisation/>
    <partenaires/>
    <clients/>
    <maaf/>
    <cta/>
    
  </main>
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
  }

}
</script>

<style>

</style>
