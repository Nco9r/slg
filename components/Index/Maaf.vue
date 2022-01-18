<template>
  <section class="maaf">
    <div class="title_maaf">
      <h3>Des travaux en toute tranquillité avec notre assurance décennale.</h3>
      <img src="~assets/img/svg/wave.svg" alt="">
    </div>
    <div class="logo_assurance">
        <img src="~assets/img/svg/logo_6.svg" alt="">
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style scoped>
.maaf {
  margin: 30px 15px 0px 15px;
  background-color: var(--baseline);
  padding: 30px;
  border-radius: 0 25px 0 25px;
}

.title_maaf h3 {
    width: 280px;
}

.logo_assurance {
    margin-top: 40px;
}


@media screen and (min-width: 1024px) {
  .title_maaf h3 {
    margin: 30px auto;
    font-size:26px;
    width: 600px;
  }

  .maaf {
    text-align: center;
    max-width: 900px;
    margin: 20px auto;
  }
}

@media screen and (min-width: 1180px) {
  .title_maaf h3 {
    margin: 30px auto;
    font-size:36px;
    width: 600px;
  }

  .maaf {
    text-align: center;
    max-width: 900px;
    margin: 20px auto;
  }
}

@media screen and (min-width: 1250px) {
  .title_maaf h3 {
    margin: 30px auto;
    font-size:34px;
    line-height: 42px;
    width: 600px;
  }

  .maaf {
    text-align: center;
    max-width: 1150px;
    margin: 20px auto;
  }
}

@media screen and (min-width: 1800px) {
  .title_maaf h3 {
    margin: 30px auto;
    font-size:34px;
    line-height: 42px;
    width: 600px;
  }

  .maaf {
    text-align: center;
    max-width: 1750px;
    margin: 20px auto;
  }
}
</style>
