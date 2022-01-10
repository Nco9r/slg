<template>
<section class="hero_banner">
    <div class="hero_img">
        <img src="~assets/img/png/home_img.jpg" alt="">
    </div>
    <div class="hero_content">
        <div class="title_hero">
            <h1>Maçonnerie, Terrassement, <span class="turquoise">Pisciniste</span> à Cestas. (33)</h1>
            <img src="~assets/img/svg/wave.svg" alt="">
        </div>
        <div class="btn">
            <p>Devis Gratuit</p>
        </div>
    </div>
    <div class="mouse">
        <img src="~assets/img/svg/mouse.svg" alt="">
    </div>
</section>
  
</template>

<script>
export default {

}
</script>

<style scoped>

/* VARIABLES */

.turquoise {
    color: var(--turquoise);
}

/* PAGE */

.hero_banner {
    overflow-x: hidden;
    overflow-y: hidden;
    position: relative;
    margin-top: 70px;
}

.hero_img img {
    width: 100%;
    object-fit: cover;
    height: 100%;

}

.hero_content {
    background-color: var(--bleu);
    margin-top: -10px;
    width: 100%;
    height: 510px;
    background-image: url('~assets/img/svg/carre.svg');
    background-size: 135%;
    padding: 10px 45px 10px 35px;
}

.title_hero h1 {
    margin-top: 30px;
    font-size: 32px;
    line-height: 46px;
    font-weight: 900;
    margin-bottom: 15px;
    color: var(--white);
}

.btn {
    margin-top: 30px;
    text-align: center;
    font-weight: 700;
    width: 250px;
    color: var(--bleu);
}

.mouse {
    position: absolute;
    bottom: 80px;
    left: 50%;
    animation: scroll 1.2s infinite ease-in-out;
}

@keyframes scroll {
    0% {
        transform: translateY(0px);
    }
    50% {
        transform: translateY(20px);
    }
    100% {
        transform: translateY(0px);
    }
}

@media screen and (min-width: 1024px) {
.hero_img img {
    width: 85%;
    object-fit: cover;
    height: 100vh;
    margin-right: -90px;
}

    .hero_content {
        position: absolute;
        width: 35%;
        height:65%;
        right: 0;
          padding: 40px 70px 40px 70px;
        bottom: -100px;
    }

    .title_hero h1 {
    margin-top: 30px;
    font-size: 52px;
    line-height: 66px;
    width: 400px;
    font-weight: 900;
    margin-bottom: 15px;
    color: var(--white);
}
}
</style>