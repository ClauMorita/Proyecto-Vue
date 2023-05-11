<template>
  <div id="app row m-0 p-0 w-100">
    <div class="row m-0 p-0 w-100 justify-content-center d-none d-sm-none d-md-block" style="background-color: black; min-height: 39px;">
      <b-nav class="nav-texto">
        <b-nav-item disabled><p class="text-light">PLAZOS DE ENTREGA</p></b-nav-item>
        <b-nav-item disabled><p class="text-light">REGIÓN METROPOLITANA: 2 A 3 DÍAS</p></b-nav-item>
        <b-nav-item disabled><p class="text-light">REGIONES: 5 A 15 DÍAS (CIERTAS ZONAS SUJETAS A EXCEPCIÓN)</p></b-nav-item>
        <b-nav-item disabled><p class="text-light">REVISAR AQUÍ</p></b-nav-item>
      </b-nav>
    </div>
    <b-navbar type="light" variant="light">
      <a class="navbar-brand"><img alt="Vue logo" src="./assets/logo.png"></a>
      <b-nav-form>
        <b-form-input class="sm-9" placeholder="Buscar por palabra clave/título/autor/ISBN"></b-form-input>
        <b-button variant="danger-light" class="my-2 my-sm-0" type="submit"><i class="fas fa-search fa-lg"></i></b-button>
      </b-nav-form>
      <i class="fas fa-map-marker-alt fa-lg"></i>
      <i class="fas fa-user fa-lg"></i>
      <i class="fas fa-shopping-cart fa-lg"></i>
    </b-navbar>

    <ul class="nav justify-content-center">
      <li class="nav-item">
        <a class="nav-link active text-dark" href="#">CATEGORÍAS</a>
      </li>
      <li class="nav-item">
        <a class="nav-link text-secondary" href="#">NOVEDADES</a>
      </li>
      <li class="nav-item">
        <a class="nav-link text-secondary" href="#">MÁS VENDIDOS</a>
      </li>
      <li class="nav-item">
        <a class="nav-link disabled text-dark">EDITORIAL CONTRAPUNTO</a>
      </li>
      <li class="nav-item">
        <a class="nav-link disabled text-dark">MOLESKINE</a>
      </li>
      <li class="nav-item">
        <a class="nav-link disabled text-dark ">LOQI</a>
      </li>
    </ul>
    <HelloWorld msg="" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
/* @media only screen and (max-width: 800px) {
  
  .nav-custom {
    display: block;
    background-color: lightblue;}
} */

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.nav-texto{
  font-size: 15px;
  justify-content: center;  
  text-align: center;
}


</style>
