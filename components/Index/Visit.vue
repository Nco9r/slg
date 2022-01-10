<template>
  <section class="visit">
    <div class="title_visit">
      <h3>Une visite préalable dédiée à l’expertise et au conseil.</h3>
      <img src="~assets/img/svg/wave.svg" alt="" />
    </div>
    <div class="content_visit">
      <p>
        Vous avez besoin d’une de nos prestations ? Nous nous tenons à votre
        disposition pour tout type d’intervention sur Bordeaux Métropole et sa
        Région.
      </p>
      <p>Devis et déplacements gratuits !</p>
    </div>
    <div class="btn">
        <p>Estimer mon projet</p>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style>
.visit {
  background-color: var(--bleu);

  padding: 50px 15px 70px 26px;
  margin-top: 60px;
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
</style>
