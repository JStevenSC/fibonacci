<template>
  <div class="carta">
    <img alt="Vue logo" src="../assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <h1>¿Qué es la sucesión de Fibonacci?</h1>
    <p class="mx-5 my-5 texto">
      ¿Alguna vez escuchaste hablar acerca de la sucesión de Fibonacci?
       ¿Imaginas una ecuación capaz de explicar matemáticamente todo en el universo? ¿Crees que semejante cosa realmente sería posible?

      Bueno, de las tantas sucesiones matemáticas que existen, ninguna es tan famosa, tan interesante y tan asombrosa como
      la que inventó Fibonacci. A lo largo de los años, hombres de ciencia, artistas de todo tipo y arquitectos, la han utilizado para trabajar, a veces a propósito y otras de forma inconsciente, pero siempre con resultados majestuosos. Te invito a conocer
      la historia detrás de todo este asunto y a que hoy aprendamos qué es la sucesión de Fibonacci. 
    </p> 

    
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  return:{
    nombre:"",
  },
  // components: {
  //   HelloWorld
  // }
}
</script>


<style>

.carta{
  background-image: url("../assets/fondo3.png");
  
}
.texto{
  text-align: justify;
}


</style>