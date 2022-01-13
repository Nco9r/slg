<template>
  <section class="news">
    <div class="block_news">
      <div class="block_left">
        <img src="~assets/img/png/mockupI.png" alt="" />
      </div>
      <div class="block_right">
        <div class="news_title">
          <p>Nouveau</p>
        </div>
        <div class="title_block">
          <h3>Automatisez votre piscine</h3>
        </div>
        <div class="content_block">
          <p>
            Avec le coffret connecté piscine tild et son application smartphone,
            faites le choix d’un bassin automatisé en toute simplicité !
          </p>
          <p>
            Entre filtration adaptée à la température de l’eau toute l’année,
            pilotage complet des projecteurs à tout moment sur le smartphone,
            tild devient votre assistant personnel rêvé.
          </p>
        </div>
        <div class="btn">
          <p>En savoir plus</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style scoped>
.block_left {
  text-align: center;
  margin-top: 50px;
  margin-bottom: 30px;
}

.block_left img {
  width: 300px;
}

.block_right {
  padding: 20px 20px 20px 26px;
  background: var(--background-gradient-rotate);
}

.block_right .news_title {
  text-transform: uppercase;
  color: var(--baseline);
  font-size: 60px;
  font-weight: 900;
  margin-left: 10px;
}

.block_right .title_block h3 {
  margin-top: -30px;
  font-size: 22px;
}

.content_block {
  margin-top: 20px;
}

.content_block p {
  line-height: 28px;
  color: var(--bleu);
  margin-bottom: 20px;
}

.btn {
  width: 250px;
  text-align: center;
  margin-top: 40px;
  color: var(--bleu);
  font-weight: bold;
  margin-bottom: 50px;
}

@media screen and (min-width: 1024px) {
  .block_news {
    display: flex;
    justify-content: space-between;
    max-width: 900px;
    margin: 100px auto;
  }

  .block_right {
    background: transparent;
    width: 55%;
  }

  .block_left {
    background: transparent;
    width: 43%;
    margin-top: 0px;
  }

  .block_left img {
    width: 100%;
  }
}
</style>
