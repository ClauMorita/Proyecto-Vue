<template>
  <div id="app row m-0 p-0 w-100">
    <div class="justify-content-center d-none d-sm-none d-md-block" style="background-color: black; min-height: 39px;">
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

    <div class="container mx-auto">
      <div class="nav-logo">
        <b-row>
          <b-navbar type="row m-0 p-0 w-100">
            <b-col>
              <a class="navbar-brand p-5"><img alt="Vue logo" src="./assets/logo.png"></a>
            </b-col>
            <b-col>
              <b-nav-form>
                <b-form-input class="" placeholder="Buscar por palabra clave/título/autor/ISBN"></b-form-input>
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
      </div>

      <div class="categorias">
        <ul class="nav justify-content-center">
          <li class="nav-item">
            <a class="nav-link text-dark font-weight-bold" href="#">CATEGORÍAS <i
                class="fa fa-angle-down cbp-submenu-aindicator"></i></a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-dark" href="#">NOVEDADES</a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-dark" href="#">MÁS VENDIDOS <i
                class="fa fa-angle-down cbp-submenu-aindicator"></i></a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-dark font-weight-bold" href="#">EDITORIAL CONTRAPUNTO</a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-dark font-weight-bold" href="#">MOLESKINE</a>
          </li>
          <li class="nav-item">
            <a class="nav-link text-dark font-weight-bold" href="#">LOQI</a>
          </li>
        </ul>
      </div>

      <div class="carousel">
        <b-carousel id="carousel-fade" style="text-shadow: 0px 0px 2px #000;" no-animation fade indicators>
          <b-carousel-slide caption="Ver todo" img-src="https://picsum.photos/1024/480/?image=10"></b-carousel-slide>
          <b-carousel-slide caption="Ver todo" img-src="https://picsum.photos/1024/480/?image=12"></b-carousel-slide>
          <b-carousel-slide caption="Comprar" img-src="https://picsum.photos/1024/480/?image=22"></b-carousel-slide>
        </b-carousel>
      </div>

      <div class="cards">
        <b-container class="bv-example-row w-100">
          <b-row>
            <b-col><img src="./assets/top.png" alt=""></b-col>
            <b-col><img src="./assets/top_infantil.png" alt=""></b-col>
            <b-col><img src="./assets/top_novedades.png" alt=""></b-col>
            <b-col><img src="./assets/top_best.png" alt=""></b-col>
          </b-row>
        </b-container>
      </div>      
      <listado-productos/>
    </div>
    <div>
    </div>
  </div>
</template>

<script>
import ListadoProductos from './components/ListadoProductos.vue';

export default {
  name: 'App',
  components:{
    'listado-productos':ListadoProductos
  },
  // mounted: function () {
    // axios
    //   .get('https://fakestoreapi.com/products')
    //   .then(productos => {
    //     console.log(productos)
    //   })
  // }
}
</script>

<style>

</style>
