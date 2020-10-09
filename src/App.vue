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
              <a href="#nosotros" v-smooth-scroll="{duration: 1000, offset: -25}">{{$t('headerInicio')}}</a>
            </li>
            <li>
              <a href="#fotos" v-smooth-scroll="{duration: 1000, offset: -25}">{{$t('headerFotos')}}</a>
            </li>
            <li>
              <a href="#aliados" v-smooth-scroll="{duration: 1000, offset: -25}">{{$t('headerAliados')}}</a>
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
          <img class="logo" alt="Logo" src="./assets/logo.svg">
          <img class="logo tablet" alt="Logo" src="./assets/logo-full.svg">
          <p>{{$t('inicioTexto1')}}</p>
          <p>{{$t('inicioTexto2')}}</p>
          <p>{{$t('inicioTexto3')}}</p>
          <p><span class="negrita">{{$t('inicioTitulo1')}}</span><br/>{{$t('inicioTexto4')}}</p>
          <p>{{$t('inicioTexto5')}}</p>
          <p><span class="negrita">{{$t('inicioTitulo2')}}</span><br/>{{$t('inicioTexto6')}}</p>
          <p>{{$t('inicioTexto7')}}</p>
          <p class="cursiva">{{$t('inicioCursiva')}}</p>
        </div>
        <div class="inicio-img">
          <img class="" alt="One Tropical Seeds" src="./assets/ots-nosotros.jpg">
        </div>
      </section>

      <section class="fotos" id="fotos">
        <img class="logo" alt="Logo" src="./assets/logo.svg">
        <div class="fotos-container">
          <img class="fotos-item" src="./assets/01.jpg" alt="One Tropical Seeds" />
          <img class="fotos-item" src="./assets/02.jpg" alt="One Tropical Seeds" />
          <img class="fotos-item" src="./assets/03.jpg" alt="One Tropical Seeds" />
          <img class="fotos-item" src="./assets/04.jpg" alt="One Tropical Seeds" />
          <img class="fotos-item" src="./assets/05.jpg" alt="One Tropical Seeds" />
          <img class="fotos-item" src="./assets/06.jpg" alt="One Tropical Seeds" />
          <img class="fotos-item" src="./assets/07.jpg" alt="One Tropical Seeds" />
          <img class="fotos-item" src="./assets/08.jpg" alt="One Tropical Seeds" />
          <img class="fotos-item" src="./assets/09.jpg" alt="One Tropical Seeds" />
          <img class="fotos-item" src="./assets/010.jpg" alt="One Tropical Seeds" />
        </div>
      </section>

      <section class="aliados" id="aliados">
        <img class="logo" alt="Logo" src="./assets/logo.svg">
        <div class="aliados-container">
          <div class="aliados-item">
            <h2 class="titulo">{{$t('aliadosTexto1')}}</h2>
            <img class="aliados-img" src="./assets/logo-laboratorio.jpg" alt="Kelab Cromatografía" />
          </div>

          <div class="aliados-item">
            <h2 class="titulo">{{$t('aliadosTexto2')}}</h2>
            <img class="aliados-img" src="./assets/logo-distribuidor.jpg" alt="Saenz Fety" />
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
              <p>Paipa, Boyacá<br>Colombia</p>
            </div>

            <div>
              <p>{{$t('contactoTxt2')}}<br>@onetropicalseeds</p>
              <div class="social-icons">
                <a href="https://www.facebook.com/onetropicalseeds/">
                  <img class="logo" alt="Logo" src="./assets/facebook.svg">
                </a>
                <a href="https://www.instagram.com/onetropicalseeds/">
                  <img class="logo" alt="Logo" src="./assets/instagram.svg">
                </a>
              </div>
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
      headerInicio: 'Nosotros',
      headerFotos: 'Fotos',
      headerAliados: 'Aliados',
      headerContacto: 'Contacto',
      inicioTitulo1: 'ICA',
      inicioTitulo2: 'Ministerio de Justicia',
      inicioTexto1: 'One Tropical Seeds S.A.S',
      inicioTexto2: 'Empresa licenciada Colombiana, ubicada en Paipa Boyacá. Cultivadores de cannabis medicinal no psicoactivo y cultivadores de fruta Nopal.',
      inicioTexto3: 'Actualmente contamos con las licencias y registros:',
      inicioTexto4: 'Registro como Unidad de Evaluación Agronómica de cannabis psicoactivo y no psicoactivo.',
      inicioTexto5: 'Registro como Productor de Semilla Seleccionada (sexual y asexual) de cannabis psicoactivo y no psicoactivo.',
      inicioTexto6: 'Licencia de cultivo no psicoactivo',
      inicioTexto7: 'Apoyamos empresas en su direccionamiento en proyectos de cultivo y producción de cannabis y otros cultivos de manera personalizada.',
      inicioCursiva: 'Empresa licenciada legalmente, no se vende ni se distribuye para consumo. Apto para mayores de 18 años.',
      aliadosTexto1: 'Laboratorio Aliado',
      aliadosTexto2: 'Distribuidor Oficial',
      contactoTitulo: 'Contáctenos y hablaremos de sus intereses',
      contactoSubtitulo: 'Contáctenos',
      contactoFormNombre: 'Nombres',
      contactoFormCel: 'Celular',
      contactoFormEmail: 'Correo',
      contactoFormMsg: 'Mensaje',
      contactoFormBtn: 'Enviar',
      contactoTxt: 'Celulares de contacto:',
      contactoTxt2: 'Encuentrenos:'
    },
    en: {
      headerInicio: 'About Us',
      headerFotos: 'Pictures',
      headerAliados: 'Allies',
      headerContacto: 'Contact Us',
      inicioTitulo1: 'ICA',
      inicioTitulo2: 'Ministry of Justice',
      inicioTexto1: 'One Tropical Seeds S.A.S',
      inicioTexto2: 'Colombian licensed company, located in Paipa Boyacá. Non-psychoactive medical cannabis growers and Nopal fruit growers.',
      inicioTexto3: 'We currently have the following licenses and registrations:',
      inicioTexto4: 'Register as an Agronomic Evaluation Unit for psychoactive and non-psychoactive cannabis.',
      inicioTexto5: 'Register as Producer of Selected Seed (sexual and asexual) of psychoactive and non-psychoactive cannabis.',
      inicioTexto6: 'Non-psychoactive cultivation license',
      inicioTexto7: 'We support companies in their direction in projects of cultivation and production of cannabis and other crops in a personalized way.',
      inicioCursiva: 'Legally licensed company, we do not sell or distribute for consumption. Suitable for people over 18 years old.',
      aliadosTexto1: 'Allied Laboratory',
      aliadosTexto2: 'Official Distributor',
      contactoTitulo: 'Contact us and we´ll talk about your interests',
      contactoSubtitulo: 'Contact us',
      contactoFormNombre: 'Name',
      contactoFormCel: 'Mobile',
      contactoFormEmail: 'Email',
      contactoFormMsg: 'Message',
      contactoFormBtn: 'Send',
      contactoTxt: 'Contact Phones:',
      contactoTxt2: 'Find Us:'
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
    font-size: 0.6em;
    font-style: italic;
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
      width: auto;
      ul {
        display: flex;
        align-items: center;
        justify-content: space-around;
        list-style-type: none;
        margin: 0;
        padding: 0;
        width: 100%;
        li {
          margin-right: 3em;
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
      margin: 0 4em;
      width: 50%;
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
      width: 50%;
      img {
        height: auto;
        width: 85%;
      }
      @media screen and (max-width: $break-tablet) {
        display: none;
      }
    }
  }
  .fotos {
    padding: 2em;
    .fotos-container {
      display: flex;
      align-items: center;
      justify-content: space-evenly;
      flex-wrap: wrap;
      .fotos-item {
        margin: 1em 0;
        height: auto;
        width: 45%;
      }
    }
  }
  .aliados {
    padding: 2em;
    .aliados-container {
      display: flex;
      align-items: center;
      justify-content: space-evenly;
      flex-wrap: wrap;
      .aliados-item {
        margin: 1em 0;
        height: auto;
        width: 45%;
        img {
          height: auto;
          width: 50%;
        }
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
      background-image: url('./assets/contacto.jpg');
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
        .social-icons {
          display: flex;
          align-items: center;
          justify-content: space-evenly;
          .logo {
            margin: 0;
            padding: 0;
          }
        }
      }
    }
  }
</style>
