<template>
  <section class="cta">
      <div class="title_cta">
          <h3>Réalisons <span class="turquoise">ensemble</span> vos projets</h3>
      </div>
      <div class="content_cta">
          <p>Obtenez un devis rapidement en nous contactant.</p>
      </div>
      <div class="btn">
            <nuxt-link to="/contact">
          <p>Devis gratuit</p>
            </nuxt-link>
      </div>
     
  </section>
</template>

<script>
export default {

}
</script>

<style scoped>

.cta {
    background-image: url('~assets/img/png/cta_img.jpg');
    margin-top: 50px;
    height: 320px;
    background-size: cover;
    text-align: center;
    padding: 40px 20px;
}

.title_cta h3 {
    color: var(--white);
    font-size: 32px;
}

.content_cta p{
    margin-top: 20px;
    margin-bottom: 20px;
    color: var(--white);
    line-height: 28px;
}

.btn {
    margin: auto;
}

@media screen and (min-width: 1024px) {
    .cta {
        background-size: 100%;
        background-position: 50%;
    }

    .title_cta h3 {
    color: var(--white);
    font-size: 42px;
    width: 500px;
    margin: 10px auto 0 auto;
    line-height: 56px;
}

.btn {
    margin: 30px auto 0 auto;
}

}

</style>