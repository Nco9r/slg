<template>
  <section class="cta">
      <div class="title_cta">
          <h3>Réalisons ensemble vos projets</h3>
      </div>
      <div class="content_cta">
          <p>Obtenez un devis rapidement en nous contactant</p>
      </div>
      <div class="btn">
          <p>Devis gratuit</p>
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
    margin-top: 100px;
    height: 400px;
    background-size: cover;
    text-align: center;
    padding: 40px 20px;
}

.title_cta h3 {
    color: var(--white);
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

</style>