<template>
  <footer>
   
    <div class="container_footer">
      <div class="infos_footer">
        <div class="logo_footer">
                  <img src="~assets/img/png/logo.png" alt="" />

          <div class="infos_contact">
            <p>contact@slgrealisation.fr</p>
            <p>+33 (0)6 83 97 65 90</p>
            <p>
              Maçonnerie, Terrassement,
              <span class="turquoise">Pisciniste</span> à Cestas, Bordeaux et sa
              Région (33).
            </p>
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
        </div>
        <div class="items_footer">
          <div class="item_footer">
            <h4>Sitemap</h4>
            <nuxt-link to="/"><p>Accueil</p></nuxt-link>
            <nuxt-link to="/services/creation-de-piscine"><p>Services</p></nuxt-link>
            <nuxt-link to="/realisations"><p>Réalisations</p></nuxt-link>
          </div>
          <div class="item_footer">
            <h4>Légales</h4>
            <nuxt-link to="/mentions-legales"><p>Mentions légales</p></nuxt-link>
            <nuxt-link to="/mentions-legales"><p>Politique de confidentialité</p></nuxt-link>
            <nuxt-link to="/mentions-legales"><p>Cookies</p></nuxt-link>
          </div>
          <div class="item_footer desktop">
            <h4>Nous suivre</h4>
          
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
      </div>
      <div class="copyright">
        <p>
          SLG réalisation SAS est une société par actions simplifiée au capital social de 5 000,00€
          immatriculée au RCS de Bordeaux (B 883 384 067) dont le siège social
          est situé au 95 Avenue du Maréchal de Lattre de Tassigny, 33610
          Cestas.
        </p>
        <div class="block_copyright">


        <p>
          © 2022 - <strong>SLGréalisation</strong> - Tous droits réservés - Siret
          : n° 883 384 067 00012 - NAF : 4399C.
        </p>
        <a href="https://rouxnicolas.fr" target="_blank">
        <p>Made w/ Nicolas ROUX</p>
        </a>
              </div>
        <div class="sociaux_desktop">
          <a href="" target="_blank"><img src="" alt="" /></a>
          <a href="" target="_blank"><img src="" alt="" /></a>
          <a href="" target="_blank"><img src="" alt="" /></a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      Sucess: false,
      error: false,
      existing: false,
      form: {
        email: '',
      },
    }
  },
  methods: {
    submit(e) {
      e.preventDefault()
      console.log({ ...this.form })

      this.$axios
        .post('https://rouxnicolas.fr/api/subscribe', { ...this.form })
        .then((res) =>
          (this.form = '')((this.Sucess = true))((this.error = false))
        )
        .catch(e)
      //   this.error = true
    },
  },
}
</script>

<style scoped>
a {
  text-decoration: none;
  color: var(--white);
}

.wave {
  overflow: hidden;
  margin-top: -50px;
  margin-bottom: -20px;
}



footer {
  background-color: var(--bleu);
  background-image: url('~assets/img/svg/plamier_2.svg');
  background-size: 75%;
  background-repeat: no-repeat;
  background-position: 150% 120%;
}

.container_footer {
  padding: 20px 20px 10px 20px;

  display: flex;
  flex-flow: row wrap;
 
  color: var(--white);
}

.infos_footer {
  margin-top: 10px;
  display: flex;
  flex-flow: row wrap;
  justify-content: left;
}

.logo_footer {
  display: flex;
  flex-flow: column;
}
.logo_footer img {
  width: 150px;
}

.infos_contact {
  margin-top: 20px;
}

.sociaux_desktop {
  display: none;
}

.sociaux {
  margin-bottom: 10px;
  margin-top: 30px;
}
.sociaux img {
  width: 25px;
  margin-right: 20px;
}

.infos_contact p {
  margin-bottom: 10px;
  font-size: 14px;
  line-height: 26px;
  color: var(--white);
}

.items_footer {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
}

.desktop {
  display: none;
}

.item_footer {
  width: 160px;
}

.item_footer h4 {
  text-transform: uppercase;
  font-size: 16px;
  margin-bottom: 20px;
  margin-top: 20px;
  font-weight: bold;
  color: var(--yellow);
}



.item_footer p {
  margin-bottom: 10px;
  font-size: 14px;
}

.item_footer .input {
  align-items: center;
  display: flex;
  margin-bottom: 30px;
}

.item_footer .input input {
  padding: 12px 24px;
  border: none;
  outline: none;
  font-family: sofia-pro, sans-serif;
  font-size: 16px;
  border-radius: 3px;
}

.item_footer .input input::placeholder {
  color: var(--gray-light);
}

.copyright {
  margin-top: 40px;
  margin-bottom: 10px;
}

.copyright p {
  font-size: 12px;
  line-height: 22px;
  margin-bottom: 10px;
  font-weight: bold;
}

@media screen and (min-width: 1024px) {

 footer {
  background-color: var(--bleu);
  background-image: url('~assets/img/svg/plamier_2.svg');
  background-size: 25%;
  background-repeat: no-repeat;
  background-position: 100% 120%;
}
  .container_footer {
    max-width: 900px;
    margin: auto;
    padding: 0;
  }

  .wave {
  overflow: hidden;
  margin-top: -50px;
  margin-bottom: -120px;
}

.wave img{
 width: 1000px;
}

  .logo_footer {
    width: 200px;
  }

  .infos_footer {
    margin-top: 30px;
    display: flex;
    flex-flow: row wrap;
      justify-content: space-between;
  }

  .logo_footer p {
    width: 170px;
  }

  .items_footer {
    margin-left: 130px;
  }

  .item_footer {
    width: 180px;
  }

  .item_footer img {
    margin-right: 20px;
  }

  hr {
    display: none;
  }

  .copyright {
    display: flex;
    width: 100%;
    justify-content: space-between;
    flex-flow: column;
  }

  .block_copyright {
    display: flex;
    justify-content: space-between;
  }
  .sociaux_desktop {
    display: flex;
    align-items: center;
  }

  .items_footer {
    display: flex;
  }

  .sociaux {
    display: none;
  }

  .sociaux_desktop img {
    margin-left: 15px;
  }
}

@media screen and (min-width: 1200px) {
  .container_footer {
    max-width: 1200px;
    margin: auto;
  }


footer {
  background-color: var(--bleu);
  background-image: url('~assets/img/svg/plamier_2.svg');
  background-size: 25%;
  background-repeat: no-repeat;
  background-position: 100% 0%;
}

  .logo_footer {
    width: 300px;
  }

  .infos_footer {
    margin-top: 30px;
    display: flex;
    flex-flow: row wrap;
    justify-content: space-between;
  }

  .logo_footer p {
    width: 220px;
  }

  .item_footer {
    width: 200px;
  }

  hr {
    display: none;
  }

  .copyright {
    display: flex;
    width: 100%;
    justify-content: space-between;
  }

  .copyright p:nth-child(1) {
    width: 600px;
  }
  .sociaux_desktop {
    display: flex;
    align-items: center;
  }

  .sociaux {
    display: none;
  }

  .sociaux_desktop img {
    margin-left: 15px;
  }
}
@media screen and (min-width: 1800px) {
  .container_footer {
    max-width: 1750px;
    margin: auto;
  }


footer {
  background-color: var(--bleu);
  background-image: url('~assets/img/svg/plamier_2.svg');
  background-size: 25%;
  background-repeat: no-repeat;
  background-position: 100% 0%;
}

  .logo_footer {
    width: 300px;
  }

  .infos_footer {
    margin-top: 30px;
    display: flex;
    flex-flow: row wrap;
    justify-content: space-between;
  }

  .logo_footer p {
    width: 220px;
  }

  .item_footer {
    width: 200px;
  }

  hr {
    display: none;
  }

  .copyright {
    display: flex;
    width: 100%;
    justify-content: space-between;
  }

  .copyright p:nth-child(1) {
    width: 600px;
  }
  .sociaux_desktop {
    display: flex;
    align-items: center;
  }

  .sociaux {
    display: none;
  }

  .sociaux_desktop img {
    margin-left: 15px;
  }
}
</style>
