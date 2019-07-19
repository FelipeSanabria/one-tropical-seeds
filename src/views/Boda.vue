<template>
  <div class="boda">
    <div class="boda-tarjeta-wrapper">
      <div class="boda-tarjeta">
        <div class="boda-titulo">
          <span class="boda-titulo-txt">DIANA</span>
          <span class="boda-titulo-txt">BRYAN</span>
        </div>
        <div class="boda-mensaje">
          <p class="boda-mensaje-titulo">¡NOS CASAMOS!</p>
          <img class="boda-img" alt="¡Nos Casamos!" src="../assets/boda-copas.svg">
          <p class="boda-mensaje-txt">TENEMOS EL AGRADO DE INVITARLOS <br/> A CELEBRAR NUESTRA BODA</p>
        </div>

        <div class="boda-lugar-fecha-wrapper">
          <div class="boda-lugar-fecha">
            <div class="boda-lugar">
              <p class="boda-lugar-fecha-titulo">Lugar</p>
              <p class="boda-lugar-fecha-txt">CLUB MILITAR DE OFICIALES</p>
              <p class="boda-lugar-fecha-txt">PAIPA, BOYACÁ</p>
            </div>

            <img class="boda-img" alt="" src="../assets/boda-planta.svg">

            <div class="boda-fecha">
              <p class="boda-lugar-fecha-titulo">Fecha & hora</p>
              <p class="boda-lugar-fecha-txt">OCTUBRE 12 - 2019</p>
              <p class="boda-lugar-fecha-txt">HORA: Por confirmar</p>
            </div>
          </div>
        </div>

        <div class="boda-traje">
          <p class="boda-titulo-2">Traje</p>
          <p>
            <span class="boda-txt-verde"><span class="titulo-verde">Mujeres:</span> Formal, no color blanco</span><br />
            <span class="boda-txt-verde"><span class="titulo-verde">Hombres:</span> Formal, colores oscuros</span>
          </p>
        </div>

        <div class="boda-sobres">
          <img class="boda-img" alt="¡Lluvia de Sobres!" src="../assets/boda-sobres.svg">
          <p class="boda-titulo-2">¡Lluvia de sobres!</p>
        </div>

        <div class="boda-recomendaciones">
          <a href="" class="boda-txt-verde">
            <span class="boda-lineas">Conoce aquí</span>
            <span>recomendaciones para alojamiento y viaje</span>
          </a>
        </div>

        <div class="boda-confirmacion">
          <p class="boda-titulo-2">Confirmación antes del 30 de agosto de 2019</p>
          <p class="boda-titulo-2">
            <countdown :time="43 * 24 * 60 * 60 * 1000">
              <template slot-scope="props">Quedan {{ props.days }} días, {{ props.hours }} horas, {{ props.minutes }} minutos, {{ props.seconds }} segundos</template>
            </countdown>
          </p>
        </div>

        <div class="boda-form">
          <p class="boda-form-titulo">UNICAMENTE SE REGISTRAN PERSONAS CON INVITACIÓN</p>
          <p class="boda-form-txt">*Favor registrarse por persona para conocer los cupos</p>
          <form class="boda-form-inner" id="boda-form" action="https://formspree.io/dianasnomali@gmail.com"
            method="POST">
            <input type="text" class="" hidden="true" name="Asunto" text="Confirmación Asistente a la Boda">
            <input type="text" class="boda-form-input" name="Nombre" placeholder="Nombre y Apellido">
            <input type="number" class="boda-form-input" name="Cedula" placeholder="Cedula">
            <button type="submit" class="boda-form-btn">ENVIAR</button>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
  //Breakpoints
  $break-tablet: 768px;
  $break-mobile: 425px;
  // Colors
  $boda-green: #12544A;
  $boda-text: #333333;
  $boda-grad: linear-gradient(to right, rgba(252, 214, 198, 1) 0%, rgba(237, 154, 126, 1) 100%);

  //Fonts
  @font-face {
    font-family: 'Didot';
    src: url('../assets/fonts/didot.woff') format('woff'),
      url('../assets/fonts/didot.ttf') format('truetype');
    font-weight: normal;
    font-style: normal;
  }

  .boda {
    background-color: $boda-green;
    background-image: url("../assets/boda-bg.svg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-family: 'Didot';
    @media screen and (max-width: $break-mobile) {
      background-size: 200%;
      background-position: top;
      background-repeat: repeat;
    }
    .boda-tarjeta-wrapper {
      background: $boda-grad;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      margin: 5em 0;
      padding: 1rem;
      width: calc(100% - 6em);
      .boda-tarjeta {
        background-color: white;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 100%;
        .boda-titulo {
          background-image: url("../assets/boda-y.svg");
          background-position: center;
          background-repeat: no-repeat;
          background-size: contain;
          display: flex;
          align-items: center;
          justify-content: space-evenly;
          margin: 2em 0;
          padding: 4em 3em 8em 3em;
          width: 75%;
          @media screen and (max-width: $break-tablet) {
            flex-direction: column;
            padding: 2em 3em 6em 3em;
          }
          @media screen and (max-width: $break-mobile) {
            padding: 2em 0 6em 0;
            width: 90%;
          }
          .boda-titulo-txt {
            font-size: 2.8em;
            font-weight: bold;
            letter-spacing: 2.5rem;
            @media screen and (max-width: $break-tablet) {
              margin: 1em 0;
            }
            @media screen and (max-width: $break-mobile) {
              letter-spacing: 1.5rem;
              text-align: center;
              width: 100%;
            }
          }
        }
        .boda-mensaje {
          display: flex;
          align-items: center;
          justify-content: center;
          flex-direction: column;
          width: 75%;
          @media screen and (max-width: $break-mobile) {
            width: 90%;
          }
          .boda-mensaje-titulo {
            font-size: 2.1em;
            color: $boda-green;
            letter-spacing: 0.5rem;
          }
          .boda-mensaje-txt {
            font-size: 1.5em;
            color: $boda-text;
            letter-spacing: 0.25rem;
          }
        }
        .boda-lugar-fecha-wrapper {
          background: $boda-grad;
          display: flex;
          flex-direction: column;
          align-items: center;
          justify-content: center;
          margin: 1em 0;
          padding: 0.5rem;
          width: 75%;
          @media screen and (max-width: $break-mobile) {
            width: 85%;
          }
          .boda-lugar-fecha {
            background-color: white;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 1em 0;
            width: 100%;
            @media screen and (max-width: $break-tablet) {
              flex-direction: column;
            }
            .boda-lugar-fecha-titulo {
              font-size: 2.1em;
              color: $boda-text;
              letter-spacing: 0.25rem;
              margin: 0.5em;
            }
            .boda-lugar-fecha-txt {
              font-size: 1.1em;
              font-style: italic;
              color: $boda-green;
              letter-spacing: 0.25rem;
              margin: 0.5em;
            }
            .boda-lugar {
              padding: 0 2em;
              width: 30%;
              @media screen and (max-width: $break-tablet) {
                width: 100%;
              }
            }
            .boda-fecha {
              padding: 0 2em;
              width: 30%;
              @media screen and (max-width: $break-tablet) {
                width: 100%;
              }
            }
          }
        }
        .boda-traje {
          display: flex;
          align-items: center;
          justify-content: center;
          flex-direction: column;
          margin: 1rem 0;
          width: 75%;
          @media screen and (max-width: $break-mobile) {
            width: 90%;
          }
        }
        .boda-sobres {
          display: flex;
          align-items: center;
          justify-content: center;
          flex-direction: column;
          margin: 1rem 0;
          width: 75%;
          @media screen and (max-width: $break-mobile) {
            width: 90%;
          }
        }
        .boda-recomendaciones {
          display: flex;
          align-items: center;
          justify-content: center;
          flex-direction: column;
          margin: 1rem 0;
          width: 75%;
          @media screen and (max-width: $break-mobile) {
            width: 90%;
          }
        }
        .boda-confirmacion {
          display: flex;
          align-items: center;
          justify-content: center;
          flex-direction: column;
          margin: 1rem 0;
          width: 75%;
          @media screen and (max-width: $break-mobile) {
            width: 90%;
          }
        }
        .boda-form {
          display: flex;
          align-items: center;
          justify-content: center;
          flex-direction: column;
          margin: 2rem 0;
          width: 75%;
          @media screen and (max-width: $break-mobile) {
            width: 90%;
          }
          .boda-form-titulo {
            color: $boda-text;
            font-size: 1.1em;
            letter-spacing: 0.25rem;
            margin: 1rem 0;
          }
          .boda-form-txt {
            color: $boda-text;
            font-size: 1em;
            letter-spacing: 0.15rem;
            margin: 0;
          }
          .boda-form-inner {
            display: flex;
            align-items: flex-end;
            justify-content: center;
            flex-direction: column;
            width: 50%;
            @media screen and (max-width: $break-tablet) {
              width: 100%;
            }
            .boda-form-input {
              border: solid 1px $boda-green;
              color: $boda-text;
              font-family: 'Didot';
              font-size: 1.4em;
              letter-spacing: 0.25rem;
              margin: 0.25rem 0;
              padding: 0.5rem 1rem;
              width: -webkit-fill-available;
              &::-webkit-inner-spin-button, &::-webkit-outer-spin-button {
                -webkit-appearance: none;
                margin: 0;
              }
            }
            .boda-form-btn {
              background: none;
              border: none;
              color: $boda-green;
              font-family: 'Didot';
              font-size: 1.4em;
              font-style: italic;
              margin: 0.25em 0;
            }
          }
        }
        .boda-titulo-2 {
          color: $boda-text;
          font-size: 2.1em;
          letter-spacing: 0.25rem;
          margin: 0.5em;
        }
        .boda-txt-verde {
          color: $boda-green;
          font-size: 1.4em;
          font-style: italic;
          letter-spacing: 0.25rem;
          text-decoration: none;
          @media screen and (max-width: $break-mobile) {
            width: 100%;
          }
          .titulo-verde {
            font-style: normal;
            font-weight: bold;
          }
        }
        .boda-lineas {
          display: flex;
          align-items: center;
          justify-content: center;
          &::after, &::before {
            content: "";
            display: inline-block;
            background: $boda-grad;
            margin: 0 1em;
            height: 4px;
            width: 100px;
            @media screen and (max-width: $break-mobile) {
              width: 70px;
            }
          }
        }
        .boda-img {
          width: 3em;
        }
      }
    }
  }
</style>

<script>
import Vue from 'vue'
import VueCountdown from '@chenfengyuan/vue-countdown'

Vue.component(VueCountdown.name, VueCountdown)

export default {
  name: 'boda'
}
</script>
