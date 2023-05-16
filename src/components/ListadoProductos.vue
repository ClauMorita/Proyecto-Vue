<template>  
<div>
<div class="card" style="width: 18rem;" v-for="(item, index) in productos" :key="index">
  <img v-bind:src= item.image>
  <div class="card-body">
    <h5 class="card-title">{{ item.title }}</h5>
    <p class="card-text">{{ item.description }}</p>
    <a href="#" class="btn btn-primary">Ver</a>
  </div>
</div>
  </div>  
      <!-- <p v-for="(item, index) in info" :key="index">Productos:{{ item.title }}</p>       -->      
</template>

<script>
import axios from "axios";

export default{
  name: 'App',
  data() {
    return {
      info:[],
      productos: []
    }
  },
  mounted(){
    axios
      .get('https://fakestoreapi.com/products')
      .then(productos => {this.productos=productos.data
      })
      
    axios.get("https://api.dailymotion.com/videos?channel=news&limit=10")
    .then(respuesta=>{this.info=respuesta.data.list
    console.log (respuesta.data.list)})  
  }   
  }

</script>