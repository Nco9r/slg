<template>
  <div>
    <div class="open">
      <img src="~assets/img/svg/wave_header.svg" alt="" />
    </div>
    <div class="bck_section">
      <section class="des_projet">
        <nuxt-link to="/realisations">
          <div class="return">
            <img src="~assets/img/svg/return.svg" alt="" />
            <p>Retour aux projets</p>
          </div>
        </nuxt-link>
        <div class="block_content">
          <div class="block_left">
            <div class="title_block">
              <h2>Le projet en détail</h2>
              <img src="~assets/img/svg/wave.svg" alt="" />
            </div>
            <div class="content_block">
              <p>{{ piscine.description }}</p>
            </div>
          </div>
          <div class="block_right">
            <div class="box">
              <img src="~assets/img/svg/points.svg" alt="" />
            </div>
            <client-only>
              <div class="block">
                <vue-tiny-slider v-bind="tinySliderOptions" ref="tinySlider">
                  <div class="box_img">
                    <img :src="getStrapiMedia(piscine.image2.url)" alt="" />
                  </div>
                  <div class="box_img">
                    <img :src="getStrapiMedia(piscine.image3.url)" alt="" />
                  </div>
                  <div class="box_img">
                    <img :src="getStrapiMedia(piscine.image4.url)" alt="" />
                  </div>
                  <div class="box_img">
                    <img :src="getStrapiMedia(piscine.image5.url)" alt="" />
                  </div>
                  <div class="box_img">
                    <img :src="getStrapiMedia(piscine.image.url)" alt="" />
                  </div>
                </vue-tiny-slider>
              </div>
            </client-only>
            <div class="slide_tiny">
              <button class="slidePrev" id="prev">
                <img src="@/assets/img/svg/arrow.svg" alt="" />
              </button>
              <button class="slideNext" id="next">
                <img src="@/assets/img/svg/arrow.svg" alt="" />
              </button>
            </div>
          </div>
        </div>
      </section>
    </div>
    <cta />
  </div>
</template>

<script>
import { getStrapiMedia } from '~/utils/medias'
import Cta from '../../../components/Index/Cta.vue'
export default {
  components: { Cta },
  async asyncData({ $strapi, params }) {
    const id = params.id
    const piscine = await $strapi.find(`terrassements/${id}`)
    return { piscine, id }
  },
  methods: {
    getStrapiMedia,
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
  data() {
    return {
      tinySliderOptions: {
        mouseDrag: true,
        loop: true,
        items: 1,
        mode: 'carousel',
        nav: false,
        autoplay: true,
        autoplayTimeout: 3500,
        speed: 700,
        autoplayButtonOutput: false,
        container: '.box_cards',
        autoplayButtonOutput: false,
        gutter: 20,
        preventScrollOnTouch: 'auto',
        controls: true,
        prevButton: '#prev',
        nextButton: '#next',
      },
    }
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

.bck_section {
  background: var(--background-gradient-rotate);
  margin-bottom: -50px;
  overflow: hidden;
}

.des_projet {
  margin-top: 100px;
  padding: 30px 26px;
}

.return {
  display: flex;
  align-items: center;
}

.return img {
  width: 6px;
  margin-right: 10px;
}

.return p {
  text-transform: uppercase;
  font-size: 12px;
  color: var(--bleu);
}

.block_content {
  margin-top: 20px;
}

.title_block h2 {
  font-size: 28px;
  line-height: 36px;
  font-weight: 900;
  color: var(--bleu);
  margin-bottom: 5px;
}

.title_block img {
  margin-bottom: 10px;
}

.content_block p {
  color: var(--bleu);
  font-size: 16px;
}

.tns-item {
  margin-right: 0px;
  margin-left: 0px;
  display: block;
}

.tns-carousel {
  display: flex;
  flex-flow: row nowrap;
  justify-content: center;
}

.box_img {
  display: block;
}

.box_img img {
  width: 100%;
  height: 300px;
  object-fit: cover;
  border-radius: 0 25px 0 25px;
}

.block_right {
  position: relative;
}

.slide_tiny {
  display: flex;
  flex-flow: row nowrap;
  justify-content: center;
  margin-top: -15px;
  margin-bottom: 25px;
  pointer-events: all;
}

/* .tns-item {
  padding: 40px 20px;
  margin-left: 25px;
  margin-right: 15px;
  text-align: center;
  width: 325px!important;
} */

.slide_tiny .slidePrev {
  border: none;
  background-color: transparent;

  display: flex;
  justify-content: center;
  align-items: center;
  margin-right: 5px;
  margin-top: 5px;
  margin-bottom: 5px;
}

.slide_tiny .slideNext {
  border: none;
  background-color: transparent;
  display: flex;
  margin-top: 5px;
  margin-bottom: 5px;
  justify-content: center;
  align-items: center;
}

.slide_tiny .slidePrev img {
  transform: rotate(180deg);
}

.block {
  margin-top: 10px;
  overflow: hidden;
}

.box {
  position: absolute;
  right: -30px;
  top: -5px;
}

.block_right {
  margin-top: 30px;
}

@media screen and (min-width: 1024px) {
  .des_projet {
    max-width: 900px;
    margin: 100px auto 50px auto;
    padding: 0;
  }

  .block_content {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .block_left {
    width: 40%;
  }

  .box_img img {
  width: 100%;
  height: 400px;
  object-fit: cover;
  margin-top: -10px;
  border-radius: 0 25px 0 25px;
}

  .block_right {
    width: 45%;
  }
}

@media screen and (min-width: 1200px) {
.des_projet {
    max-width: 1150px;
    margin: 100px auto 50px auto;
  }
}
</style>
