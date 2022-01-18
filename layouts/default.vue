<template>
  <div>
    <the-header />
    <nuxt />
    <the-footer />
  </div>
</template>

<script>
import TheFooter from '../components/Default/TheFooter.vue'
import TheHeader from '../components/Default/TheHeader.vue'

export default {
  components: {
    TheHeader,
    TheFooter,
  },
}
</script>

<style>
html {
  font-family: 'Work sans', Times, serif;
  font-weight: 400;
  font-style: normal;
  line-height: 28px;
  font-size: 16px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
 
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

:root {
  --white: #fff;
  --bleu: #064a57;
  --turquoise: #46b3bc;
  --turquoise-light: #b0e2e6;
  --yellow: #fbcc2e;
  --orange: #CE7D5F;
  --baseline: #f1f5f6;
  --background-gradient: linear-gradient(
    180deg,
    rgb(229, 250, 250) 0%,
    rgba(255, 255, 255, 1) 100%
  );
  --background-gradient-rotate: linear-gradient(
    180deg,
    rgba(255, 255, 255, 1) 0%,
    rgb(229, 250, 250)  100%
  );
}

a {
  text-decoration: none;
  color: var(--bleu);
}

h3 {
  font-weight: bold;
  font-size: 26px;
  line-height: 36px;
  color: var(--bleu);
}

.btn {
 background: var(--yellow);
  padding: 12px 18px;
  border-radius: 0 25px 0 25px;
  width: 250px;
  margin-top: 30px;
  text-align: center;
  color: var(--bleu);
  font-weight: bold;
  cursor: pointer;
  transition: all .3s;
}

.btn:hover {
  background: var(--turquoise);
  
}


.btn_light {
  background-color: transparent;
  padding: 12px 18px;
  border-radius: 0 25px 0 25px;
  width: 250px;
  text-align: center;
  color: var(--bleu);
  border: 1Px solid var(--bleu);
  font-weight: bold;
}

.turquoise {
  color: var(--turquoise);
}

.label p {
  color: var(--bleu);
  font-weight: bold;
  font-size: 14px;
}

.label p::after {
  content: '*';
  color: var(--white);
  margin-left: 2px;
  margin-top: -2px;
}

input {
  padding: 16px 26px;
  border: 1px solid var(--bleu);
  border-radius: 0 25px 0 25px;
  width: 100%;
  font-family: 'Work sans', sans-serif;
  font-size: 16px;
  color: var(--bleu);
  margin-bottom: 20px;
  outline-color: var(--bleu);
}

textarea {
  padding: 16px 26px;
    border: 1px solid var(--bleu);

  border-radius: 0 25px 0 25px;
  width: 100%;
  font-family: 'Work sans', sans-serif;
  font-size: 16px;
  color: var(--bleu);
  margin-bottom: 20px;
  outline-color: var(--bleu);
}

select {
  padding: 16px 26px;
    border: 1px solid var(--yellow);

  background-color: var(--bleu);
  border-radius: 0 25px 0 25px;
  width: 100%;
  font-family: 'Work sans', sans-serif;
  font-size: 16px;
  color: var(--yellow);
  margin-bottom: 20px;
  background-image: url('~assets/img/svg/angle.svg');
  background-repeat: no-repeat;
  background-position: 90% 52%;
  background-size: 25px;
  font-weight: bold;
  appearance: none;
  outline-color: var(--turquoise);
}

@media screen and (min-width: 768px) {
 
}
</style>
