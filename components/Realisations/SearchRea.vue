<template>
  <section class="search">
      <div class="title_search">
          <h2>Catégories</h2>
          <img src="~assets/img/svg/wave.svg" alt="">
      </div>
      <div class="box_categorie">
          <div class="item_categorie" @click="piscine = true, maconnerie = false, ter = false" :class="{active : piscine}">
              <p>Piscine</p>
          </div>
             <div class="item_categorie" @click="piscine = false, maconnerie = true, ter = false" :class="{active : maconnerie}">
              <p>Maçonnerie</p>
          </div>
           <div class="item_categorie" @click="piscine = false, maconnerie = false, ter = true" :class="{active : ter}">
              <p>Terrassement</p>
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
    }

}
</script>

<style scoped>

.title_search {
    padding: 10px 26px 5px 26px;
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
  transition: all .3s;
}

.item_categorie p {
    width: 150px;
}

.active {
     background-color: var(--yellow);
     color: var(--bleu);
     font-weight: bold;
}
</style>