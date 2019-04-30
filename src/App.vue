<template>
  <div id="app">
    <div class="landing">
      <header class="navbar">
        <div class="left">
          <img class="logo-header" alt="Logo Header" src="./assets/logo-full.svg">
          <img class="logo-header tablet" alt="Logo Header" src="./assets/logo.svg">
        </div>

        <div class="right">
          <ul>
            <li>
              <a href="#inicio" v-smooth-scroll="{duration: 1000, offset: -25}">{{$t('headerInicio')}}</a>
            </li>
            <li>
              <a href="#servicios" v-smooth-scroll="{duration: 1000, offset: -25}">{{$t('headerServicios')}}</a>
            </li>
            <li>
              <a href="#contacto" v-smooth-scroll="{duration: 1000, offset: -25}">{{$t('headerContacto')}}</a>
            </li>
            <li>
              <div class="vertical-line"></div>
            </li>
            <li>
              <a href="#" @click="$i18n.locale = 'es'">ES</a>
            </li>
            <li>
              <a href="#" @click="$i18n.locale = 'en'">EN</a>
            </li>
          </ul>
        </div>
      </header>

      <section class="inicio" id="inicio">
        <div class="inicio-txt">
          <p class="negrita">{{$t('inicioRes1')}}</p>
          <p class="negrita">{{$t('inicioRes2')}}</p>
          <p class="negrita">{{$t('inicioRes3')}}</p>
          <img class="logo" alt="Logo" src="./assets/logo.svg">
          <img class="logo tablet" alt="Logo" src="./assets/logo-full.svg">
          <p>{{$t('inicioTxt1')}}</p>
          <p>{{$t('inicioTxt2')}}</p>
          <p class="cursiva">{{$t('inicioCursiva')}}</p>
        </div>
        <div class="inicio-img">
          <img class="" alt="One Tropical Seeds" src="./assets/foto-home-1.jpg">
        </div>
      </section>

      <section class="servicios" id="servicios">
        <img class="logo" alt="Logo" src="./assets/logo.svg">
        <h2 class="titulo">{{$t('serviciosTitulo')}}</h2>
        <p>{{$t('serviciosSubtitulo')}}</p>
        <div class="servicios-grid">
          <div class="servicios-item">
            <span class="cursiva">{{$t('serviciosProduccion')}}</span>
            <img class="logo" alt="Producción" src="./assets/produccion.svg">
          </div>

          <div class="servicios-item">
            <span class="cursiva">{{$t('serviciosLicencias')}}</span>
            <img class="logo" alt="Licencias" src="./assets/licencias.svg">
          </div>

          <div class="servicios-item">
            <span class="cursiva">{{$t('serviciosCultivo')}}</span>
            <img class="logo" alt="Cultivo" src="./assets/cultivo.svg">
          </div>

          <div class="servicios-item">
            <span class="cursiva">{{$t('serviciosConsultoria')}}</span>
            <img class="logo" alt="Consultoría" src="./assets/consultorias.svg">
          </div>
        </div>
      </section>

      <section class="contacto" id="contacto">
        <img class="logo" alt="Logo" src="./assets/logo.svg">
        <h2 class="titulo">{{$t('contactoTitulo')}}</h2>
        <div class="contacto-cont">
          <div class="contacto-form">
            <form class="contacto-form-inner" id="contact-form" action="https://formspree.io/dianasnomali@gmail.com" method="POST">
              <h3 class="subtitulo">{{$t('contactoSubtitulo')}}</h3>
              <input type="text" class="contacto-input" name="Nombre" :placeholder="$t('contactoFormNombre')">
              <input type="number" class="contacto-input" name="Celular" :placeholder="$t('contactoFormCel')">
              <input type="email" class="contacto-input" name="Correo" :placeholder="$t('contactoFormEmail')">
              <textarea class="contacto-textarea" name="mensaje" :placeholder="$t('contactoFormMsg')" cols="30" rows="10"></textarea>
              <button type="submit" class="btn-form">{{$t('contactoFormBtn')}}</button>
            </form>
          </div>

          <div class="contacto-txt">
            <img class="logo" alt="Logo" src="./assets/logo.svg">
            <div>
              <p>{{$t('contactoTxt')}}</p>
              <p>(+57) 1 3134717940<br>(+57) 1 3173668903</p>
              <p>Colombia</p>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import vueSmoothScroll from 'vue-smooth-scroll'
import VueAnalytics from 'vue-analytics'
import VueI18n from 'vue-i18n'

Vue.use(vueSmoothScroll)

Vue.use(VueAnalytics, {
  id: 'UA-134258083-1'
})

Vue.use(VueI18n)

export const i18n = new VueI18n({
  locale: 'es',
  fallbackLocale: 'es',
  messages: {
    es: {
      headerInicio: 'Inicio',
      headerServicios: 'Servicios',
      headerContacto: 'Contacto',
      inicioRes1: 'Contamos con las resoluciones:',
      inicioRes2: 'Resolución No.00005059 - Registro como Unidad de Evaluación Agronómica de cannabis psicoactivo y no psicoactivo.',
      inicioRes3: 'Resolución No.00005060 - Registro como Productor de Semilla Seleccionada (sexual y asexual) de cannabis psicoactivo y no psicoactivo.',
      inicioTxt1: 'En One Tropical Seeds S.A.S, tenemos como objetivo principal la realización de consultorías y acompañamiento a pequeños, medianos y grandes productores, compañías, y proyectos en su etapa inicial, en la consecución de licencias para el cultivo de Cannabis, la transformación y legalización de sus productos derivados en Colombia. Además, realizamos asesorías en cultivos de plantas aromáticas, manejo, recomendaciones y obtención de subproductos con fines medicinales y terapéuticos.',
      inicioTxt2: 'Direccionamos proyectos de producción y exportación de frutas desde Colombia y hacia el exterior de manera personalizada con nuestro equipo de profesionales calificados para tal fin.',
      inicioCursiva: 'Hacemos de la naturaleza un estilo de vida',
      serviciosTitulo: 'Nuestros Servicios',
      serviciosSubtitulo: 'Asesoría en producción, cultivo, documentación para licencias y consultorías en plantas medicinales y Cannabis.',
      serviciosProduccion: 'Produccion',
      serviciosLicencias: 'Licencias',
      serviciosCultivo: 'Cultivo',
      serviciosConsultoria: 'Consultoria',
      contactoTitulo: 'La verdadera esencia de la naturaleza',
      contactoSubtitulo: 'Contáctenos',
      contactoFormNombre: 'Nombres',
      contactoFormCel: 'Celular',
      contactoFormEmail: 'Correo',
      contactoFormMsg: 'Mensaje',
      contactoFormBtn: 'Enviar',
      contactoTxt: 'Celulares de contacto:'
    },
    en: {
      headerInicio: 'Home',
      headerServicios: 'Services',
      headerContacto: 'Contact Us',
      inicioRes1: 'We have the following resolutions:',
      inicioRes2: 'Resolution # 00005059 - Registration as an Agronomic Evaluation Unit of psychoactive and non-psychoactive cannabis.',
      inicioRes3: 'Resolution # 00005060 - Registration as Selected Seed Producer (sexual and asexual) of psychoactive and non-psychoactive cannabis.',
      inicioTxt1: 'At One Tropical Seeds S.A.S, our main objective is to carry out consultancies and support to small, medium and large producers, companies and projects in their initial stage, in obtaining licenses for the cultivation of Cannabis and the transformation and legalization of their derivates in Colombia. In adittion, we provide advice on aromatic plant crops, management, recommendations and byproduct obtaining for medicinal and therapeutic purposes.',
      inicioTxt2: 'We manage fruit production and export projects from Colombia and abroad in a personalized way with our team of qualified professionals.',
      inicioCursiva: 'We make nature a lifestyle',
      serviciosTitulo: 'Our Services',
      serviciosSubtitulo: 'Assistance on production, cultivation and documentation for licenses and consultancies in medicianl plants and Cannabis.',
      serviciosProduccion: 'Production',
      serviciosLicencias: 'Licenses',
      serviciosCultivo: 'Crop',
      serviciosConsultoria: 'Consultancies',
      contactoTitulo: 'The true essence of nature',
      contactoSubtitulo: 'Contact us',
      contactoFormNombre: 'Name',
      contactoFormCel: 'Mobile',
      contactoFormEmail: 'Email',
      contactoFormMsg: 'Message',
      contactoFormBtn: 'Send',
      contactoTxt: 'Contact Phones:'
    }
  }
})

export default {
  name: 'app',
  i18n,
  methods: {
    track () {
      this.$ga.page('/')
    }
  }
}

i18n.locale = 'es'
</script>

<style lang="scss">
  //Breakpoints
  $break-tablet: 768px;
  $break-mobile: 425px;
  // Colors
  $color-green: #517c42;
  $color-text: #333333;
  $color-bg: #ffffff;
  //Fonts
  @font-face {
    font-family: 'Ginette';
    src:  url('./assets/fonts/ginette.woff2') format('woff2'),
          url('./assets/fonts/ginette.woff') format('woff'),
          url('./assets/fonts/ginette.ttf') format('truetype');
    font-weight: normal;
    font-style: normal;
  }

  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: $color-text;
    letter-spacing: 1px;
    transition: all ease .33s;
  }
  body {
    margin: 0;
    scroll-behavior: smooth;
  }
  .mobile {
    display: none;
    @media screen and (max-width: $break-mobile) {
      display: block !important;
    }
  }
  .tablet {
    display: none;
    @media screen and (max-width: $break-tablet) {
      display: block !important;
    }
  }
  .cursiva {
    font-family: 'Ginette';
  }
  .negrita {
    font-weight: 700;
  }
  .logo {
    width: 2rem;
    margin: 0.5em 0;
  }
  .titulo {
    font-family: 'Book Antiqua', Times, serif;
    font-size: 2em;
    font-weight: 400;
    letter-spacing: 3px;
    text-transform: uppercase;
    font-style: italic;
  }
  .navbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 2em 4em;
    @media screen and (max-width: $break-mobile) {
      padding: 2em;
    }
    .left {
      .logo-header {
        width: 200px;
        height: auto;
        @media screen and (max-width: $break-tablet) {
          display: none;
          width: 30px;
        }
      }
      @media screen and (max-width: $break-mobile) {
        display: none;
      }
    }
    .right {
      width: 30%;
      ul {
        display: flex;
        align-items: center;
        justify-content: space-around;
        list-style-type: none;
        margin: 0;
        padding: 0;
        width: 100%;
        li {
          a {
            color: $color-text;
            text-decoration: none;
            &:hover {
              color: $color-green;
            }
          }
        }
      }
      @media screen and (max-width: $break-tablet) {
        width: 80%;
      }
      @media screen and (max-width: $break-mobile) {
        width: 100%;
      }
    }
    .vertical-line {
      background-color: rgba($color: $color-text, $alpha: 0.5);
      height: 20px;
      width: 1px;
    }
  }
  .inicio {
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    padding: 2em;
    .inicio-txt {
      margin: 0 2em;
      width: 30%;
      .cursiva {
        font-size: 1.5em;
      }
      img {
        @media screen and (max-width: $break-tablet) {
          display: none;
        }
        &.tablet {
          margin: 0 auto 2em auto;
          width: 50%;
          @media screen and (max-width: $break-mobile) {
            width: 85%;
          }
        }
      }
      @media screen and (max-width: $break-tablet) {
        width: 85%;
        .cursiva {
          margin: 2em auto 0 auto;
          width: 60%;
        }
      }
      @media screen and (max-width: $break-mobile) {
        margin: 0;
        width: 100%;
        .cursiva {
          margin: 2em auto 0 auto;
          width: 85%;
        }
      }
    }
    .inicio-img {
      margin: 0 2em;
      img {
        height: 100%;
        width: auto;
      }
      @media screen and (max-width: $break-tablet) {
        display: none;
      }
    }
  }
  .servicios {
    padding: 2em;
    .servicios-grid {
      display: flex;
      align-items: center;
      justify-content: space-evenly;
      margin: 2em 0;
      @media screen and (max-width: $break-tablet) {
        flex-wrap: wrap;
      }
      .servicios-item {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        @media screen and (max-width: $break-tablet) {
          width: 40%;
          margin-bottom: 3em;
        }
        .cursiva {
          font-size: 1.5em;
        }
        .logo {
          margin-top: 1em;
          width: 50%;
          @media screen and (max-width: $break-tablet) {
            width: 35%;
          }
          @media screen and (max-width: $break-mobile) {
            width: 50%;
          }
        }
      }
    }
  }
  .contacto {
    padding: 2em;
    @media screen and (max-width: $break-mobile) {
      padding: 0;
    }
    .contacto-cont {
      background-image: url('./assets/foto-home-2.jpg');
      background-position: center;
      background-size: cover;
      background-repeat: no-repeat;
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      height: 100%;
      margin: 0 2em;
      padding: 0 4em 4em 4em;
      @media screen and (max-width: $break-tablet) {
        flex-direction: column-reverse;
      }
      @media screen and (max-width: $break-mobile) {
        margin: 0;
        padding: 0 2em 2em 2em;
      }
      .contacto-form {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: flex-start;
        padding: 3em 0;
        width: 65%;
        @media screen and (max-width: $break-tablet) {
          width: 100%;
        }
        .contacto-form-inner {
          display: flex;
          flex-direction: column;
          align-items: flex-start;
          justify-content: flex-start;
          width: 90%;
          @media screen and (max-width: $break-tablet) {
            width: 100%;
          }
          .contacto-input {
            background: none;
            border: 1px solid $color-bg;
            border-radius: 10px;
            color: $color-bg;
            font-size: 0.8em;
            margin: 1em 0;
            padding: 10px;
            width: -webkit-fill-available;
            &::placeholder {
              color: $color-bg;
              letter-spacing: 1px;
            }
            &:focus {
              outline: none;
            }
            &::-webkit-inner-spin-button, &::-webkit-inner-spin-button {
              -webkit-appearance: none;
              margin: 0;
            }
          }
          .contacto-textarea {
            background: none;
            border: 1px solid #ffffff;
            border-radius: 10px/30px;
            color: $color-bg;
            font-size: 0.8em;
            margin: 0.5em 0;
            padding: 10px;
            resize: none;
            width: -webkit-fill-available;
            &::placeholder {
              color: #ffffff;
              letter-spacing: 1px;
            }
            &:focus {
              outline: none;
            }
          }
          .btn-form {
            background: #ffffff;
            border: none;
            border-radius: 10px/25px;
            font-family: 'Book Antiqua', Times, serif;
            font-size: 1em;
            letter-spacing: 2px;
            margin: 1em 0;
            padding: 10px 3em;
            align-self: flex-end;
          }
        }
        .subtitulo {
          color: #ffffff;
          font-family: 'Book Antiqua', Times, serif;
          font-size: 1em;
          font-weight: 400;
          letter-spacing: 3px;
          text-transform: uppercase;
        }
      }
      .contacto-txt {
        background: #ffffff;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 100%;
        padding: 10em 1em;
        width: 35%;
        @media screen and (max-width: $break-tablet) {
          padding: 5em 0;
          width: 100%;
        }
        .logo {
          margin: 2em 0;
        }
      }
    }
  }
</style>
