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
              <a href="#inicio" v-smooth-scroll="{duration: 1000, offset: -25}">Inicio</a>
            </li>
            <li>
              <a href="#servicios" v-smooth-scroll="{duration: 1000, offset: -25}">Servicios</a>
            </li>
            <li>
              <a href="#contacto" v-smooth-scroll="{duration: 1000, offset: -25}">Contacto</a>
            </li>
          </ul>
        </div>
      </header>

      <section class="inicio" id="inicio">
        <div class="inicio-txt">
          <img class="logo" alt="Logo" src="./assets/logo.svg">
          <img class="logo tablet" alt="Logo" src="./assets/logo-full.svg">
          <p>En One Tropical Seeds S.A.S, tenemos como objetivo principal la realización de consultorías y acompañamiento a pequeños, medianos y grandes productores, compañías, y proyectos en su etapa inicial, en la consecución de licencias para el cultivo de Cannabis, la transformación y legalización de sus productos derivados en Colombia. Además, realizamos asesorías en cultivos de plantas aromáticas, manejo, recomendaciones y obtención de subproductos con fines medicinales y terapéuticos.</p>
          <p>Direccionamos proyectos de producción y exportación de frutas desde Colombia y hacia el exterior de manera personalizada con nuestro equipo de profesionales calificados para tal fin.</p>
          <p class="cursiva">Hacemos de la naturaleza un estilo de vida</p>
        </div>
        <div class="inicio-img">
          <img class="" alt="One Tropical Seeds" src="./assets/foto-home-1.jpg">
        </div>
      </section>

      <section class="servicios" id="servicios">
        <img class="logo" alt="Logo" src="./assets/logo.svg">
        <h2 class="titulo">Nuestros Servicios</h2>
        <p>Asesoría en producción, cultivo, documentación para licencias y consultorías en plantas medicinales y Cannabis.</p>
        <div class="servicios-grid">
          <div class="servicios-item">
            <span class="cursiva">Produccion</span>
            <img class="logo" alt="Producción" src="./assets/produccion.svg">
          </div>

          <div class="servicios-item">
            <span class="cursiva">Licencias</span>
            <img class="logo" alt="Licencias" src="./assets/licencias.svg">
          </div>

          <div class="servicios-item">
            <span class="cursiva">Cultivo</span>
            <img class="logo" alt="Cultivo" src="./assets/cultivo.svg">
          </div>

          <div class="servicios-item">
            <span class="cursiva">Consultoria</span>
            <img class="logo" alt="Consultoría" src="./assets/consultorias.svg">
          </div>
        </div>
      </section>

      <section class="contacto" id="contacto">
        <img class="logo" alt="Logo" src="./assets/logo.svg">
        <h2 class="titulo">La verdadera esencia de la naturaleza</h2>
        <div class="contacto-cont">
          <div class="contacto-form">
            <form class="contacto-form-inner" id="contact-form" action="https://formspree.io/dianasnomali@gmail.com" method="POST">
              <h3 class="subtitulo">Contáctenos</h3>
              <input type="text" class="contacto-input" name="Nombre" placeholder="Nombres">
              <input type="number" class="contacto-input" name="Celular" placeholder="Celular">
              <input type="email" class="contacto-input" name="Correo" placeholder="Correo">
              <textarea class="contacto-textarea" name="Mensaje" placeholder="Mensaje" cols="30" rows="10"></textarea>
              <button type="submit" class="btn-form">Enviar</button>
            </form>
          </div>

          <div class="contacto-txt">
            <img class="logo" alt="Logo" src="./assets/logo.svg">
            <div>
              <p>Celulares de contacto:</p>
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

Vue.use(vueSmoothScroll)

export default {
  name: 'app'
}
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
  .logo {
    width: 2rem;
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
