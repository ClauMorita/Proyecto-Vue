<template>  
    <div class="content">
      <p>Productos:{{productos }}</p>
    </div>  
</template>

<script>
import axios from "axios";

export default {
  name: 'App',
  mounted: function () {
    axios
      .get('https://fakestoreapi.com/products')
      .then(productos => {
        console.log(productos)
      })
  }
}
</script>