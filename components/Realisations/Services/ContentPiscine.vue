<template>
  <section class="content_piscine">
      <div class="block_content">
          <div class="content_right">
              <div class="content_img">
                  <img src="~assets/img/svg/icon_piscine.svg" alt="">
                  <img src="~assets/img/png/contentpiscine_img.jpg" alt="">
                  <div class="rec"></div>
              </div>
          </div>
          <div class="content_left">
              <div class="title_left">
                  <p>Services</p>
                  <h3>Création de piscine</h3>
              </div>
              <div class="content">
                  <p>Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur </p>
                  <p>Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur </p>
              </div>
              <div class="btn_light">
                  <p>Nos réalisations</p>
              </div>
              <div class="btn">
                  <p>Devis gratuit</p>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {

}
</script>

<style scoped>
.content_piscine {
    margin-top: 30px;
    margin-bottom: 100px;
    overflow: hidden;

}


.block_content {
    padding: 10px 26px;
}

.content_img {
    position: relative;
}

.content_img img:nth-child(1) {
    position: absolute;
    top: -10px;
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

.title_left p{
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

.btn {
    margin: 0px auto ;
    width: 100%;
}

.btn_light {
    margin: 30px auto 20px auto;
    width: 100%;
}
</style>