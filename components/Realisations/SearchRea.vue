<template>
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
    <div class="box_projets" v-if="piscine">
      <div class="projet">
        <img src="~assets/img/png/img_2.jpg" alt="" />
        <div class="bck"></div>
        <div class="cta_projet">
          <p>Voir le projet</p>
          <p>Piscine en block polystyrène</p>
        </div>
      </div>
      <div class="projet">
        <img src="~assets/img/png/home_img.jpg" alt="" />
        <div class="bck"></div>
        <div class="cta_projet">
          <p>Voir le projet</p>
          <p>Piscine traditionnelle</p>
        </div>
      </div>
      <div class="projet">
        <img src="~assets/img/png/img_3.jpg" alt="" />
        <div class="bck"></div>
        <div class="cta_projet">
          <p>Voir le projet</p>
          <p>Piscine en block polystyrène</p>
        </div>
      </div>
      
    </div>
    <div class="box_projets" v-if="maconnerie">
      
      <div class="projet">
        <img src="~assets/img/png/img_4.jpg" alt="" />
        <div class="bck"></div>
        <div class="cta_projet">
          <p>Voir le projet</p>
          <p>Terrain de pétanque</p>
        </div>
      </div>
    </div>
     <div class="box_projets" v-if="ter">
      
      <div class="projet">
        <img src="~assets/img/png/img_4.jpg" alt="" />
        <div class="bck"></div>
        <div class="cta_projet">
          <p>Voir le projet</p>
          <p>Terrain de pétanque</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      piscine: true,
      maconnerie: false,
      ter: false,
    }
  },
}
</script>

<style scoped>
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
  background-color: var(--yellow);
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

.projet {
  margin-bottom: 20px;

  position: relative;
}

.bck {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 9px;
  border-radius: 0 25px 0 25px;
  background: linear-gradient(
    180deg,
    rgba(255, 255, 255, 0) 0%,
    rgba(6, 73, 86, 0.9) 80%
  );
  z-index: 3;
}

.cta_projet {
  position: absolute;
  left: 30px;
  bottom: 40px;
  z-index: 4;
}

.cta_projet p {
  color: var(--white);
  font-weight: bold;
  margin-bottom: -5px;
}

.cta_projet p:nth-child(2) {
  color: var(--white);
  font-size: 14px;
  font-weight: 400;
}
</style>
