<template>
  <div>
    <the-header/>
    <nuxt/>
    <the-footer/>
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
  border: 7px solid var(--white);
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
  --baseline: #f1f5f6;
  --background-gradient: linear-gradient(
    180deg,
    rgb(235, 250, 250) 0%,
    rgba(255, 255, 255, 1) 100%
  );
  --background-gradient-rotate: linear-gradient(
    180deg,
    rgba(255, 255, 255, 1) 0%,
    rgb(235, 250, 250) 100%
  );
}

h3 {
  font-weight: bold;
  font-size: 26px;
  line-height: 36px;
  color: var(--bleu);
}

.btn {
  background-color: var(--yellow);
  padding: 12px 18px;
  border-radius: 0 25px 0 25px;
}

.turquoise {
  color: var(--turquoise);
}
</style>
