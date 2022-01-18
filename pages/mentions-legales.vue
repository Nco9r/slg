<template>
  <main>
      <hero-mentions/>
      <content-mention/>
  </main>
</template>

<script>
import ContentMention from '../components/MetionsLegales/ContentMention.vue'
import HeroMentions from '../components/MetionsLegales/HeroMentions.vue'

export default {
  components: { HeroMentions, ContentMention },

}
</script>

<style>

</style>