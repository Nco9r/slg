<template>
  <section class="form_contact">
    <div class="block_form">
      <div class="top_form">
        <div class="top_left">
          <img src="~assets/img/svg/wave.svg" alt="" />
          <img src="~assets/img/svg/wave.svg" alt="" />
          <h2
            data-aos="fade-up"
            data-aos-offset="10"
            data-aos-delay="50"
            data-aos-duration="900"
          >
            Vous souhaitez un devis personnalisé ou une simple demande de
            renseignements ?
          </h2>
        </div>
        <div
          class="top_right"
          data-aos="fade-up"
          data-aos-offset="10"
          data-aos-delay="70"
          data-aos-duration="900"
        >
          <p>
            Nous sommes en mesure de répondre à tous vos besoins en matière de
            création de piscine de A à Z, de maçonnerie générale ou de
            terrassement. N’hésitez pas à remplir notre formulaire. Intervention
            possible sur Bordeaux Métropole et dans sa région.
          </p>
        </div>
      </div>
      <div class="form">
        <form>
          <div class="label_form">
            <div class="label">
              <p>Nom</p>
              <input type="text" />
            </div>
            <div class="label">
              <p>Prénom</p>
              <input type="text" />
            </div>
            <div class="label">
              <p>Email</p>
              <input type="email" />
            </div>
            <div class="label">
              <p>Téléphone</p>
              <input type="phone" />
            </div>
            <div class="label">
              <p>Code postal ou ville</p>
              <input type="text" />
            </div>
            <div class="label">
              <p>Nature de la demande</p>
              <select name="" id="">
                <option value="" selected disabled>Choisir</option>
                <option value="piscine">Piscine</option>
                <option value="maçonnerie">Maçonnerie</option>
                <option value="terrassement">Terrassement</option>
                <option value="presse">Presse</option>
                <option value="hello">Dire bonjour</option>
              </select>
            </div>
            <div class="label textarea">
              <p>Votre demande</p>
              <textarea cols="30" rows="10"></textarea>
            </div>
            <div class="check">
              <div class="box_check">
                <input type="checkbox" @click="checkbox = !checkbox" />
              </div>
              <div class="content">
                <p>
                  En soumettant ce formulaire, j'accepte que les données
                  transmises soient exploitées par slg realisation dans le cadre
                  de ma prise de contact.
                </p>
              </div>
            </div>
            <div class="btn" :class="{ opacity: !checkbox }">
              <p>Soumettre</p>
            </div>
          </div>
        </form>
      </div>
    </div>
  </section>
</template>

<script>
import aosMixin from '~/mixins/aos'
export default {
  data() {
    return {
      checkbox: false,
    }
  },
  mixins: [aosMixin]
}
</script>

<style scoped>
.form_contact {
  background-color: var(--turquoise);
  background-image: url('~assets/img/svg/carre.svg');
  background-size: 135%;
  padding-bottom: 50px;
}

.top_form {
  padding: 50px 10px 20px 26px;
}

.top_left {
  display: flex;
  flex-flow: column;
}

.top_left img {
  width: 140px;
  margin-bottom: 10px;
}

.top_left h2 {
  color: var(--bleu);
  line-height: 34px;
  margin-top: 20px;
}

.top_right p {
  color: var(--white);
  margin-top: 20px;
}

.form {
  padding: 20px 26px 0 26px;
}

.check {
  display: flex;
  flex-flow: row;
}

.box_check {
  width: 50px;
}

.content p {
  font-size: 12px;
  line-height: 18px;
  color: var(--white);
  margin-left: 20px;
}

input[type='checkbox' i] {
  border: 2px solid var(--white) !important;
  width: 30px !important;
  height: 30px !important;
  padding: 0;
  border-radius: 50%;
  -webkit-appearance: none;
  outline: none;
  transition: all 0.3s;
}

input[type='checkbox' i]:checked {
  background-color: var(--yellow) !important;
  width: 15px;
  background-image: url('~assets/img/svg/check.svg');
  height: 15px;

  -webkit-appearance: none;
  display: flex;

  transition: all 0.3s;
}

input[type='checkbox' i]:checked::after {
  background-color: var(--yellow) !important;
  width: 15px;
  height: 15px;
  font-weight: bold;
  margin: 2px auto;

  display: flex;
}

.btn {
  margin: 20px 0;
  transition: all 0.3s;
}

.opacity {
  background-color: rgb(230, 230, 230);
  color: rgb(192, 192, 192);
  pointer-events: none;
  opacity: 0.5;
}

@media screen and (min-width: 1024px) {
  .block_form {
    max-width: 900px;
    margin: -15px auto 50px auto;
  }

  .form_contact {
    padding-bottom: 30px;
  }

  .top_form {
    padding-top: 100px;
    display: flex;
    flex-flow: row;
    align-items: center;
    justify-content: space-between;
  }

  .top_left {
    width: 50%;
  }

  .top_right {
    width: 50%;
    margin-top: 30px;
  }

  .form {
    max-width: 800px;
    margin: 30px auto;
  }

  .label_form {
    display: flex;
    flex-flow: row wrap;
    align-items: center;
    justify-content: space-between;
  }

  .label {
    width: 47%;
  }

  .textarea {
    width: 100%;
  }

  .content p {
    font-size: 14px;
    line-height: 22px;
    color: var(--white);
    margin-left: 20px;
  }
}
</style>
