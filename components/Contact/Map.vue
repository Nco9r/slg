<template>
  <section class="map">
      <div class="title_map">
          <h3>Nous trouver</h3>
          <img src="~assets/img/svg/wave.svg" alt="">
      </div>
 <a href="https://www.google.com/maps/place/Slgrealisation/@44.7567425,-0.7371421,15z/data=!4m5!3m4!1s0x0:0xa0c815c1940cf19a!8m2!3d44.7567425!4d-0.7371421" target="_blank">
      <div class="img_map">
          <img src="~assets/img/svg/points.svg" alt="">
         
          <img src="~assets/img/png/map.jpg" alt="">
        
          <div class="rec_right"></div>
      </div>
      </a>
  </section>
</template>

<script>
export default {

}
</script>

<style scoped>

.map {
    margin-top: 30px;
    padding: 20px 26px 20px 26px;
    margin-bottom: 100px;
    overflow: hidden;
}

.img_map {
    margin-top: 50px;
    position: relative;
}

.img_map img:nth-child(2){ 
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.img_map img:nth-child(1){ 
    position: absolute;
    left: -20px;
    width: 200px;
    z-index: -1;
    margin-top: -20px;
}

.rec_right{ 
    position: absolute;
    right: -50px;
    background-color: var(--turquoise);
    height: 100px;
    width: 100px;
    z-index: -1;
    bottom: -20px;
}
</style>