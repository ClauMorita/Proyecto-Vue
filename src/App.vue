<template>
  <div id="app row m-0 p-0 w-100">
    <div class="row m-0 p-0 w-100 justify-content-center d-none d-sm-none d-md-block"
      style="background-color: black; min-height: 39px;">
      <b-nav class="nav-texto">
        <b-nav-item disabled>
          <p class="text-light m-1 pr-5 border-right">PLAZOS DE ENTREGA</p>
        </b-nav-item>
        <b-nav-item disabled>
          <p class="text-light m-1 pr-5 border-right">REGIÓN METROPOLITANA: 2 A 3 DÍAS</p>
        </b-nav-item>
        <b-nav-item disabled>
          <p class="text-light m-1 pr-5 border-right">REGIONES: 5 A 15 DÍAS (CIERTAS ZONAS SUJETAS A EXCEPCIÓN)</p>
        </b-nav-item>
        <b-nav-item disabled>
          <p class="text-light m-1">REVISAR AQUÍ</p>
        </b-nav-item>
      </b-nav>
    </div>

    <div class="container mx-auto" style="margin-left: ;">
      <b-row class="text-center">
        <b-navbar type="light row m-0 p-0 w-100 " variant="light">
          <b-col>
            <a class="navbar-brand p-5"><img alt="Vue logo" src="./assets/logo.png"></a>
          </b-col>
          <b-col cols="6" md="auto">
            <b-nav-form>
              <b-form-input class="sm-9" placeholder="Buscar por palabra clave/título/autor/ISBN"></b-form-input>
              <b-button variant="dark-light" class="my-2 my-sm-0" type="submit"><i
                  class="fas fa-search fa-lg"></i></b-button>
            </b-nav-form>
          </b-col>
          <b-col>
            <i class="fas fa-map-marker-alt fa-lg p-3"></i>
            <i class="fas fa-user fa-lg p-3"></i>
            <i class="fas fa-shopping-cart fa-lg p-3"></i>
          </b-col>
        </b-navbar>
      </b-row>

      <ul class="nav justify-content-center">
        <li class="nav-item">
          <b-dropdown text="CATEGORÍAS" variant="outline-dark" class="m-2">
            <b-dropdown-item href="#">Action</b-dropdown-item>
            <b-dropdown-item href="#">Another action</b-dropdown-item>
            <b-dropdown-item href="#">Something else here</b-dropdown-item>
          </b-dropdown>
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
      <div>
        <b-carousel id="carousel-fade" style="text-shadow: 0px 0px 2px #000" fade indicators img-width="1024"
          img-height="480">
          <b-carousel-slide caption="First Slide" img-src="https://picsum.photos/1024/480/?image=10"></b-carousel-slide>
          <b-carousel-slide caption="Second Slide" img-src="https://picsum.photos/1024/480/?image=12"></b-carousel-slide>
          <b-carousel-slide caption="Third Slide" img-src="https://picsum.photos/1024/480/?image=22"></b-carousel-slide>
        </b-carousel>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios"

export default {
  name: 'App',
  mounted: function () {
    axios.get('https://fakestoreapi.com/products').then(productos => {
      console.log(productos)
    })
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

.nav-texto {
  font-size: 15px;
  justify-content: center;
  text-align: center;
  /* border-left: 1px solid white; */
}
</style>
