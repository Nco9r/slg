<template>
  <header>
    <div class="top_header">
      <p>Demande de devis gratuit - 06 14 64 58 48</p>
    </div>
    <div class="header_mobile">
      <div class="logo_header">
        <img src="~assets/img/png/logo.png" alt="" />
      </div>
      <div class="hamburger_header" @click="open = !open">
        <img src="~assets/img/svg/hamburger.svg" alt="" />
      </div>
      <transition name="open" appear>
        <div class="box_items_header" v-if="open">
          <div class="close" @click="open = !open">
            <img src="~assets/img/svg/close.svg" alt="" />
          </div>
          <div class="items_header">
            <div class="title_items">
              <p>Découvrez slgrealisation</p>
              <hr />
            </div>
            <div class="items" @click="open = !open">
              <nuxt-link to="/">
                <p>Accueil</p>
              </nuxt-link>
              <nuxt-link to="/services/creation-de-piscine">
                <p>Nos services</p>
              </nuxt-link>
              <nuxt-link to="/realisations">
                <p>Nos réalisations</p>
              </nuxt-link>
            </div>
            <nuxt-link to="/contact">
              <div class="btn" @click="open = !open">
                <p>Contact</p>
              </div>
            </nuxt-link>
            <div class="sociaux">
              <a href="" target="_blank">
                <img src="~assets/img/svg/fb.svg" alt="" />
              </a>
              <a href="" target="_blank">
                <img src="~assets/img/svg/insta.svg" alt="" />
              </a>
              <a href="" target="_blank">
                <img src="~assets/img/svg/in.svg" alt="" />
              </a>
            </div>
          </div>

          <div class="wave_header">
            <img src="~assets/img/svg/wave_header.svg" alt="" />
          </div>
          <div class="palmier">
            <img src="~assets/img/svg/palmier.svg" alt="" />
          </div>
          <div class="palmier_2">
            <img src="~assets/img/svg/plamier_2.svg" alt="" />
          </div>
        </div>
      </transition>
    </div>
    <div class="header_desktop">
      <div class="desktop">
        <div class="block_header">
          <div class="block_left">
            <img src="~assets/img/png/logo.png" alt="" />
          </div>
          <div class="block_right">
            <div class="item_desktop">
              <nuxt-link to="/">
                <p>Accueil</p>
              </nuxt-link>
              <nuxt-link to="/services/creation-de-piscine">
                <p>Nos services</p>
              </nuxt-link>
               <nuxt-link to="/realisations">
              <p>Nos réalisations</p>
               </nuxt-link>
               <nuxt-link to="/contact">
              <div class="btn">
                <p>Contact</p>
              </div>
               </nuxt-link>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      open: false,
    }
  },
}
</script>

<style scoped>
a {
  text-decoration: none;
}

.top_header {
  position: fixed;
  top: 0;
  left: 0;
  background: linear-gradient(
    90deg,
    rgba(251, 204, 46, 1) 0%,
    rgba(255, 216, 0, 1) 100%
  );
  right: 0;
  z-index: 10;
  padding: 10px 25px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 30px;
}

.top_header p {
  font-size: 12px;
  font-weight: bold;
  color: var(--bleu);
}

.header_mobile {
  position: fixed;

  box-shadow: rgb(48 41 41 / 4%) 0px 2px 2px 1px;
  top: 30px;
  left: 0;
  background-color: var(--white);
  right: 0;
  z-index: 10;
  padding: 25px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 70px;
}


.header_desktop {
  display: none;
}

.logo_header img {
  width: 120px;
}

.box_items_header {
  position: fixed;

  top: 0;
  left: 0;
  background-color: var(--bleu);
  right: 0;
  bottom: 0;
  z-index: 12;
  overflow: hidden;
}

.items_header {
  padding: 0 40px;
  margin-top: 100px;
}

.title_items p {
  font-size: 12px;
  text-transform: uppercase;
  font-weight: bold;
  color: var(--turquoise);
}

.title_items hr {
  width: 100%;
  margin-top: 7px;
  height: 2px;
  border: none;
  background-color: var(--turquoise);
}

.items {
  margin-top: 40px;
}

.items p {
  color: var(--white);
  margin-bottom: 20px;
  font-weight: bold;
  opacity: 0;
  font-size: 20px;
  animation: move 0.6s ease-in-out;
  animation-fill-mode: forwards;
  animation-delay: 0.1s;
}

.items p:nth-child(2) {
  animation-delay: 0.2s;
}

.items p:nth-child(3) {
  animation-delay: 0.3s;
}

@keyframes move {
  from {
    opacity: 0;
    transform: translateY(15px);
  }
  to {
    opacity: 1;
    transform: translateY(0px);
  }
}

.sociaux {
  margin-bottom: 10px;
  margin-top: 50px;
  z-index: 2;
}
.sociaux img {
  width: 25px;
  margin-right: 20px;
}

@keyframes bounce {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translatey(-10px) rotate(-5deg);
  }
  100% {
    transform: translateY(0);
  }
}

@keyframes bounce_2 {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translatey(-30px) rotate(10deg);
  }
  100% {
    transform: translateY(0);
  }
}

.palmier {
  position: absolute;
  bottom: -10px;
  left: -50px;
  -webkit-animation: bounce 3.5s;
  animation: bounce 3.5s;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-timing-function: ease-in-out;
  animation-timing-function: ease-in-out;
}

.palmier img {
  width: 200px;
}
.palmier_2 {
  position: absolute;
  bottom: 10px;
  right: -57px;
  -webkit-animation: bounce_2 2.5s;
  animation: bounce_2 3.5s;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-timing-function: ease-in-out;
  animation-timing-function: ease-in-out;
}

.palmier_2 img {
  width: 180px;
}

.wave_header {
  position: absolute;
  bottom: -90px;
  left: 0px;
  animation: move_wave 0.6s ease-in-out;
  animation-fill-mode: forwards;
  right: 0px;
}

@keyframes move_wave {
  from {
    transform: translateY(90px);
  }
  to {
    transform: translateY(0px);
  }
}

.close {
  position: absolute;
  top: 30px;
  right: 30px;
}

@keyframes open {
  from {
    transform: translateX(100%);
  }
  to {
    transform: translateX(0%);
  }
}

@keyframes close {
  from {
    transform: translateX(0%);
  }
  to {
    transform: translateX(100%);
  }
}

.open-enter-active {
  animation: open 0.5s;
}



@media screen and (min-width: 1024px) {
  .header_mobile {
    display: none;
  }

  .header_desktop {
    display: flex;
  }

  .desktop {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 12;
    box-shadow: rgb(48 41 41 / 4%) 0px 2px 2px 1px;
    background-color: var(--white);
  }

  .block_header {
    max-width: 900px;
    margin: 30px auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .block_left img {
    width: 130px;
  }

  .block_right .item_desktop {
    display: flex;
    align-items: center;
  }

  .block_right .item_desktop p {
    display: flex;
    align-items: center;
    margin: 0 15px;
    text-transform: uppercase;
    font-size: 12px;
    font-weight: bold;
    color: var(--bleu);
  }

  .btn {
    width: 150px;
    padding: 8px 12px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: var(--bleu);
    font-weight: bold;
  }

  .btn {
    width: 150px;
    padding: 8px 12px;
    text-align: center;
    color: var(--bleu);
    font-weight: bold;
    margin: auto;
    text-align: center;
  }
}

@media screen and (min-width: 1200px) {
  .header_mobile {
    display: none;
  }

  .header_desktop {
    display: flex;
  }

  .desktop {
    position: fixed;
    top: 0;

    left: 0;
    right: 0;
    z-index: 10;
    background-color: var(--white);
  }

  .block_header {
    max-width: 1150px;
    margin: 30px auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .block_left img {
    width: 130px;
  }

  .block_right .item_desktop {
    display: flex;
    align-items: center;
  }

  .block_right .item_desktop p {
    display: flex;
    align-items: center;
    margin: 0 15px;
    font-size: 12px;
    font-weight: bold;
    color: var(--bleu);
    transition: all .2s;
  }


  .block_right .item_desktop p:hover {
   
    color: var(--turquoise);
  }

  .btn {
    width: 150px;
    padding: 8px 12px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: var(--bleu);
    font-weight: bold;
  }

  .btn {
    width: 150px;
    padding: 8px 12px;
    text-align: center;
    color: var(--bleu);
    font-weight: bold;
    margin: auto;
    text-align: center;
  }
}

@media screen and (min-width: 1800px) {
 .block_header {
    max-width: 1750px;
    margin: 30px auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
</style>
