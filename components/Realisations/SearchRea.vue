<template>
<div class="box_bck">
  <section class="search">
    <div class="title_search">
      <h2>Catégories</h2>
      <img src="~assets/img/svg/wave.svg" alt="" />
    </div>
    <div class="box_categorie">
      <div
        class="item_categorie"
        @click=";(piscine = true), (maconnerie = false), (ter = false)"
        :class="{ active: piscine }"
      >
        <p>Piscine</p>
      </div>
      <div
        class="item_categorie"
        @click=";(piscine = false), (maconnerie = true), (ter = false)"
        :class="{ active: maconnerie }"
      >
        <p>Maçonnerie</p>
      </div>
      <div
        class="item_categorie"
        @click=";(piscine = false), (maconnerie = false), (ter = true)"
        :class="{ active: ter }"
      >
        <p>Terrassement</p>
      </div>
    </div>
    <transition name="open" appear>
      <div class="box_projets" v-if="piscine">
        <div class="projet" v-for="p in piscines" :key="p.id">
          <nuxt-link :to="`/realisations/piscines/${p.id}`">
            <img :src="getStrapiMedia(p.image.url)" alt="" />
            <div class="bck"></div>
            <div class="cta_projet">
              <div class="icon_projet">
                <img src="~assets/img/svg/pelle.svg" alt="" />
                <p>{{ p.titre }}</p>
              </div>
              <div class="icon_projet">
                <p>Voir le projet</p>
              </div>
            </div>
          </nuxt-link>
        </div>
      </div>
    </transition>
    <transition name="open" appear>
      <div class="box_projets" v-if="maconnerie">
        <div class="projet" v-for="p in maconneries" :key="p.id">
          <nuxt-link :to="`/realisations/piscines/${p.id}`">
            <img :src="getStrapiMedia(p.image.url)" alt="" />
            <div class="bck"></div>
            <div class="cta_projet">
              <div class="icon_projet">
                <img src="~assets/img/svg/pelle.svg" alt="" />
                <p>{{ p.titre }}</p>
              </div>
              <div class="icon_projet">
                <p>Voir le projet</p>
              </div>
            </div>
          </nuxt-link>
        </div>
      </div>
    </transition>
    <transition name="open" appear>
      <div class="box_projets" v-if="ter">
        <div class="projet" v-for="p in terrassements" :key="p.id">
          <nuxt-link :to="`/realisations/piscines/${p.id}`">
            <img :src="getStrapiMedia(p.image.url)" alt="" />
            <div class="bck"></div>
            <div class="cta_projet">
              <div class="icon_projet">
                <img src="~assets/img/svg/pelle.svg" alt="" />
                <p>{{ p.titre }}</p>
              </div>
              <div class="icon_projet">
                <p>Voir le projet</p>
              </div>
            </div>
          </nuxt-link>
        </div>
      </div>
    </transition>
  </section>
</div>
</template>

<script>
import { getStrapiMedia } from '~/utils/medias'
export default {
  props: ['piscines', 'maconneries', 'terrassements'],
  data() {
    return {
      piscine: true,
      maconnerie: false,
      ter: false,
    }
  },
  methods: {
    getStrapiMedia,
  },
}
</script>

<style scoped>

.box_bck {
  background: var(--background-gradient-rotate);
}

.search {
  margin-bottom: -50px;
  padding-bottom: 50px;
}
.title_search {
  padding: 10px 26px 5px 26px;
  margin-top: 20px;
}

.title_search h2 {
  font-size: 18px;
  color: var(--bleu);
}

.title_search img {
  width: 70px;
  margin-bottom: 10px;
}

.box_categorie {
  padding: 0 0 0 26px;
  display: flex;
  flex-flow: row nowrap;
  overflow: scroll;
  margin-top: -10px;
}

.box_categorie::-webkit-scrollbar {
  display: none;
}

.item_categorie {
  background-color: var(--baseline);
  padding: 8px 16px;
  border-radius: 0 25px 0 25px;
  text-align: center;
  margin-right: 10px;
  color: gray;
  font-size: 14px;
  font-weight: bold;
  transition: all 0.3s;
}

.item_categorie p {
  width: 150px;
}

.active {
  background: linear-gradient(
    90deg,
    rgba(251, 204, 46, 1) 0%,
    rgba(255, 216, 0, 1) 100%
  );
  color: var(--bleu);
  font-weight: bold;
}

.box_projets {
  display: flex;
  margin: 40px 26px 30px 26px;
  flex-flow: column;
}

.projet img {
  width: 100%;
  border-radius: 0 25px 0 25px;
  z-index: 2;
}

.icon_projet {
  display: flex;
  flex-flow: row;
  justify-content: flex-start;
  align-items: center;
}

.icon_projet img {
  width: 25px;
  border-radius: 0px;
  margin-right: 10px;
}

.projet {
  margin-bottom: 20px;

  position: relative;
}

.bck {
  position: absolute;
  top: 0px;
  left: 0;
  right: 0;
  bottom: 9px;
  border-radius: 0 25px 0 25px;
  background: linear-gradient(
    180deg,
    rgba(255, 255, 255, 0) 0%,
    rgba(6, 73, 86, 0.7) 80%
  );
  z-index: 3;
}

.cta_projet {
  position: absolute;
  left: 30px;
  bottom: 30px;
  z-index: 4;
}

.cta_projet p {
  color: var(--white);
  font-weight: bold;
  margin-bottom: -5px;
}

.cta_projet p:nth-child(2) {
  color: var(--white);
  font-size: 12px;
  font-weight: 400;
  text-transform: uppercase;
}

@keyframes open {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes close {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}

.open-enter-active {
  animation: open 1s;
}

.open-leave-active {
  animation: close 1s;
}

@media screen and (min-width: 1024px) {
  .search {
    max-width: 900px;
    margin-top: 50px auto;
  }
}

@media screen and (min-width: 1250px) {
  .search {
    max-width: 1200px;
    margin-top: 50px auto;
  }
}

@media screen and (min-width: 1800px) {
  .search {
    max-width: 1700px;
    margin-top: 50px auto;
  }
}
</style>
