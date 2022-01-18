<template>
  <section class="baseline">
    <div class="baseline_first">
      <p>Piscine</p>

      <p>lyner</p>

      <p>beton</p>

      <p>petanque</p>
      <p>Piscine</p>

      <p>lyner</p>

      <p>beton</p>

      <p>petanque</p>
      <p>Piscine</p>

      <p>lyner</p>

      <p>beton</p>

      <p>petanque</p>
    </div>
    <div class="baseline_second">
      <p>Piscine</p>
      <p>lyner</p>
      <p>Terrassement</p>
      <p>maçonnerie</p>
      <p>Piscine</p>
      <p>lyner</p>
      <p>Terrassement</p>
      <p>maçonnerie</p>
      <p>Piscine</p>
      <p>lyner</p>
      <p>Terrassement</p>
      <p>maçonnerie</p>
    </div>
  </section>
</template>

<script>
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/dist/ScrollTrigger'
gsap.registerPlugin(ScrollTrigger)

export default {
  mounted() {
    gsap.to('.baseline_first', {
      scrollTrigger: {
        trigger: '.baseline_first',
        start: '-10% 110%',
        end: 'top',
        scrub: true,
        toggleActions: 'restart pause reverse pause',
      },
      x: 600,
    }),
      gsap.to('.baseline_second', {
        scrollTrigger: {
          trigger: '.baseline_second',
          start: '-10% 110%',
          end: 'top',
          scrub: true,
          toggleActions: 'restart pause reverse pause',
        },
        x: -600,
      })
  },
}
</script>

<style scoped>
.baseline {
  overflow: hidden;
  height: 180px;
  margin-top: 30px;
}

.baseline_first {
  display: flex;
  flex-flow: row nowrap;
  margin-left: -900px;
}

.baseline_first p {
  color: var(--baseline);
  font-size: 50px;
  line-height: 50px;
  text-transform: uppercase;
  margin-left: 7px;
  margin-right: 7px;
  font-weight: 900;
}

.baseline_first img {
  width: 20px;
}

.baseline_second {
  display: flex;
  flex-flow: row nowrap;
  margin-left: 400px;
}

.baseline_second p {
  color: var(--baseline);
  font-size: 50px;
  line-height: 50px;
  text-transform: uppercase;

  font-weight: 900;
  margin-left: 7px;
  margin-right: 7px;
}

@media screen and (min-width: 1024px) {
  .baseline {
    margin-top: 60px;
    margin-bottom: 110px;
  }

  .baseline_first {
      margin-left: -1300px;
  }

  .baseline_second {
      margin-left: -200px;
  }

  .baseline_first p {
    font-size: 80px;
    line-height: 80px;
  }

  .baseline_second p {
    font-size: 80px;
    line-height: 80px;
  }
}

@media screen and (min-width: 1024px) {
  .baseline {
    margin-top: 60px;
    margin-bottom: 70px;
  }

  .baseline_first {
      margin-left: -1300px;
  }

  .baseline_second {
      margin-left: -200px;
  }

  .baseline_first p {
    font-size: 80px;
    line-height: 80px;
  }

  .baseline_second p {
    font-size: 80px;
    line-height: 80px;
  }
}
</style>
