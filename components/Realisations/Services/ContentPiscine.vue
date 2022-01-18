<template>
  <section class="content_piscine">
    <div class="block_content">
      <div class="content_right">
        <div class="content_img">
          <img src="~assets/img/svg/icon_piscine.svg" alt="" />
          <img src="~assets/img/png/contentpiscine_img.jpg" alt="" />
          <div class="rec"></div>
        </div>
      </div>
      <div class="content_left">
        <div class="title_left">
          <p>Services</p>
          <h3>Création de piscine</h3>
        </div>
        <div class="content">
          <p>
            SLGrealisation vous propose la réalisation de
            <span class="turquoise">piscine traditionnelle</span> (maçonnerie)
            toute taille fond incliné ou droit. De plus, ils vous proposent
            également la création de
            <span class="turquoise">piscine en block polystyrène</span>. Le but
            de la piscine en block polystyrène est de construire une piscine en
            béton armé sans utiliser les banches en bois ou métal ni les
            traditionnels blocs à bancher en ciment. Celle-ci peut vous être
            également proposé de toute taille et fond incliné ou droit.
          </p>
          <p>
            De plus, nous vous proposons également
            <span class="turquoise">l'entretien</span> et le remplacement des
            <span class="turquoise">accessoires</span> de votre piscine comme
            les skimmers, les refoulement ou la filtration. Nous pouvons
            également installer ou remplacer votre lyner.
          </p>
        </div>
        <div class="btn_block">
          <div class="btn_light">
            <nuxt-link to="/realisations">
              <p>Nos réalisations</p>
            </nuxt-link>
          </div>
          <div class="btn">
            <nuxt-link to="/realisations">
              <p>Devis gratuit</p>
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style scoped>
.content_piscine {
  margin-top: 30px;
  margin-bottom: 100px;
  overflow: hidden;
}

.turquoise {
  font-weight: bold;
}

.block_content {
  padding: 10px 26px;
}

.content_img {
  position: relative;
}

.content_img img {
  height: 300px;
  width: 100%;
  border-radius: 0 25px 0 25px;

  object-fit: cover;
}

.content_img img:nth-child(1) {
  position: absolute;
  top: -10px;
  width: 70px;
  height: 70px;
  left: -20px;
}

.content_img .rec {
  position: absolute;
  bottom: -20px;
  right: -30px;
  z-index: -1;
  width: 200px;
  height: 200px;
  background-color: var(--turquoise);
}

.content_img img:nth-child(2) {
  width: 100%;
}

.content_left {
  margin-top: 70px;
}

.title_left p {
  text-transform: uppercase;
  font-size: 62px;
  font-weight: 900;
  color: var(--baseline);
  margin-left: 20px;
}

.title_left h3 {
  margin-top: -30px;
  font-size: 24px;
}

.content {
  margin-top: 30px;
}

.content p {
  line-height: 28px;
  color: var(--bleu);
  margin-bottom: 20px;
}

.btn_block {
  margin-top: 50px;
}

.btn {
  margin: 0px auto;
  width: 100%;
}

.btn_light {
  margin: 30px auto 20px auto;
  width: 100%;
}

@media screen and (min-width: 1024px) {
  .content_piscine {
    max-width: 900px;
    margin: 0px auto;
  }

  .block_content {
    display: flex;
    flex-flow: row-reverse;
    justify-content: space-between;
    align-items: center;
    padding: 0;
    position: relative;
  }

  .content_left {
    width: 46%;
  }

  .content_right {
    width: 46%;
  }

  .content_img img {
    height: 450px;
    width: 100%;
    border-radius: 0 25px 0 25px;
    object-fit: cover;
  }

  .content_img .rec {
    display: none;
  }

  .btn_block {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 10px;
    margin-bottom: 50px;
    flex-flow: row-reverse;
  }

  .btn {
    width: 200px;
    margin-top: 15px;
  }

  .btn_light {
    width: 200px;
  }
}

@media screen and (min-width: 1250px) {
  .content_piscine {
    max-width: 1200px;
    margin: 0px auto;
  }
  .title_left h3 {
    margin-top: -30px;
    font-size: 32px;
  }

  .title_left p {
    text-transform: uppercase;
    font-size: 82px;
    font-weight: 900;
    color: var(--baseline);
    margin-left: 20px;
  }

  .content p {
    line-height: 32px;
    font-size: 18px;
    width: 500px;
    color: var(--bleu);
    margin-bottom: 20px;
  }

  .content_img img {
    height: 550px;
    width: 100%;
    border-radius: 0 25px 0 25px;
    object-fit: cover;
  }

  .btn_block {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    margin-top: 10px;
    margin-bottom: 50px;
    flex-flow: row-reverse;
  }

  .btn {
    width: 200px;
    margin: 0;
  }

  .btn_light {
    width: 200px;
    margin: 20px;
  }
}
@media screen and (min-width: 1800px) {
  .content_piscine {
    max-width: 1700px;
    margin: 0px auto;
  }
}
</style>
