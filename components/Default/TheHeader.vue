<template>
  <header>
    <div class="header_mobile">
      <div class="logo_header">
        <img src="~assets/img/png/logo.png" alt="" />
      </div>
      <div class="hamburger_header" @click="open = !open">
        <img src="~assets/img/svg/hamburger.svg" alt="" />
      </div>
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
          <div class="items">
            <p>Accueil</p>
            <p>Nos services</p>
            <p>Nos réalisations</p>
          </div>
          <div class="btn">
            <p>Contact</p>
          </div>
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
      </div>
    </transition>
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
.header_mobile {
  position: fixed;
  top: 0;
  left: 0;
  background-color: var(--white);
  right: 0;
  z-index: 10;
  padding: 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 70px;
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
  animation-delay: .1s;
}

.items p:nth-child(2) {
    animation-delay: .2s;
}

.items p:nth-child(3) {
    animation-delay: .3s;
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
}
.sociaux img {
  width: 25px;
  margin-right: 20px;
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

.open-leave-active {
  animation: close 0.5s;
}
</style>
