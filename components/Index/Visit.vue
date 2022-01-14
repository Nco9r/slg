<template>
  <section class="visit">
    <div class="title_visit">
      <h3   data-aos="fade-up"
          data-aos-offset="10"
          data-aos-delay="50"
          data-aos-duration="900">Une visite préalable dédiée à l’expertise et au conseil.</h3>
      <img   data-aos="fade-up"
          data-aos-offset="10"
          data-aos-delay="50"
          data-aos-duration="900" src="~assets/img/svg/wave.svg" alt="" />
    </div>
    <div class="content_visit">
      <p   data-aos="fade-up"
          data-aos-offset="10"
          data-aos-delay="60"
          data-aos-duration="900">
        Vous avez besoin d’une de nos prestations ? Nous nous tenons à votre
        disposition pour tout type d’intervention sur Bordeaux Métropole et sa
        Région.
      </p>
      <p   data-aos="fade-up"
          data-aos-offset="10"
          data-aos-delay="70"
          data-aos-duration="900">Devis et déplacements gratuits !</p>
    </div>
    <div class="btn"   data-aos="fade-up"
          data-aos-offset="10"
          data-aos-delay="80"
          data-aos-duration="900">
        <p>Estimer mon projet</p>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style scoped>
.visit {
  background-color: var(--bleu);

  padding: 30px 15px 40px 26px;
  margin-top: 30px;
  background-image: url('~assets/img/svg/carre.svg');
  background-size: 135%;
  color: var(--white);
}

.title_visit h3 {
    color: var(--white);
    width: 300px;
}

.content_visit p {
    margin-top: 20px;
    line-height: 28px;
}

.btn {
    width: 250px;
    text-align: center;
    margin-top: 40px;
    color: var(--bleu);
    font-weight: bold;
}

@media screen and (min-width: 1024px) {
    .visit {
        text-align: center;
  background-size: 75%;

    }


.title_visit h3 {
    color: var(--white);
    width: 600px;
    font-size: 34px;
    line-height: 46px;
    margin: 20px auto;
}

.content_visit p {
    margin-top: 20px;
    line-height: 28px;
    margin: 20px auto;
    width: 600px;

}

.btn {
    margin: 50px auto 10px auto;
}
}
</style>
