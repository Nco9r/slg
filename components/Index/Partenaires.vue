<template>
  <section class="partenaires">
      <div class="box">
          <img src="~assets/img/svg/logo_1.svg" alt="">
          <img src="~assets/img/svg/logo_2.svg" alt="">
          <img src="~assets/img/svg/logo_3.svg" alt="">
          <img src="~assets/img/svg/logo_4.svg" alt="">
          <img src="~assets/img/svg/logo_5.svg" alt="">
           <img src="~assets/img/svg/logo_1.svg" alt="">
          <img src="~assets/img/svg/logo_2.svg" alt="">
          <img src="~assets/img/svg/logo_3.svg" alt="">
          <img src="~assets/img/svg/logo_4.svg" alt="">
          <img src="~assets/img/svg/logo_5.svg" alt="">
           <img src="~assets/img/svg/logo_1.svg" alt="">
          <img src="~assets/img/svg/logo_2.svg" alt="">
          <img src="~assets/img/svg/logo_3.svg" alt="">
          <img src="~assets/img/svg/logo_4.svg" alt="">
          <img src="~assets/img/svg/logo_5.svg" alt="">
            <img src="~assets/img/svg/logo_1.svg" alt="">
          <img src="~assets/img/svg/logo_2.svg" alt="">
          <img src="~assets/img/svg/logo_3.svg" alt="">
          <img src="~assets/img/svg/logo_4.svg" alt="">
          <img src="~assets/img/svg/logo_5.svg" alt="">
      </div>
  </section>
</template>

<script>
export default {

}
</script>

<style scoped>

.partenaires {
    margin: 100px 0;
    overflow: hidden;
}

.box {
    display: flex;
    flex-flow: row nowrap;
    align-items: center;
    animation: slide 55s infinite linear;
}

@keyframes slide {
    0% {
        transform: translateX(0)
    }
     100% {
        transform: translateX(-1000%)
    }
}

.box img {
    width: 200px;
    margin-right: 50px;
}

</style>