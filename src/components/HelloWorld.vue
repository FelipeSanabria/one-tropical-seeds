<template>
  <div class="hello">
    <h1 class="titulo">En construcci?n.</h1>
    <p>Puedes contactarnos en nuestras redes sociales.</p>
    <div class="redes">
      <a href="https://wa.me/573173668903" target="_blank"><i class="fab fa-whatsapp"></i></a>
      <a href="https://www.facebook.com/onetropicalseeds/" target="_blank"><i class="fab fa-facebook-f"></i></a>
      <a href="https://www.instagram.com/onetropicalseeds/" target="_blank"><i class="fab fa-instagram"></i></a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .titulo {
    font-size: 2em;
    font-family: 'Book Antiqua', Times, serif;
  }
  .redes {
    margin: 2em 0;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    a {
      color: #517c42;
      font-size: 1.25em;
      text-decoration: none;
    }
  }
</style>
