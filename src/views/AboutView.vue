<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h2 class="text-center mb-3">Vue Get Full Date and Time Example</h2>
        <ul class="list-group">
          <li class="list-group-item" v-show="fecha"><strong>Fecha:</strong> {{ fecha }}</li>
          <li class="list-group-item" v-show="time"><strong>Time:</strong> {{ time }}</li>
          <li class="list-group-item" v-show="fulldatetime"><strong>Full Date:</strong> {{ fulldatetime }}</li>
        </ul>
        
        <button @click="semillas()">segundos</button>
        
        <h1> {{ mostrar}}</h1>
      
        <h4> {{ 'semilla1=' }} {{ part1}}</h4>
        <h4> {{ 'semilla2=' }} {{ part2}}</h4>
        <h4> {{ 'Repetir=' }} {{ repetir}}</h4>
        <h4> {{ fibonacci }} </h4>

    <!-- <p>{{ $store.state.firstName }} {{ $store.state.lastName }}</p> -->
  </div>
</template>


<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  data(){
    return{
      mostrar:'',
      fecha: '',
      time: '',
      year: '',
      timestamp: '',
      fulldatetime: '',
      minutos:'',
      segundos:'',
      segundos1:'',
      part1:'',
      part2:'',
      repetir:'',
      fibonacci: [],
    }
  },
    methods: {

    reloj(){
      return  setInterval(this.mostar, 1000);
    },
    mostar(){
      this.mostrar=new Date().toLocaleTimeString();

    },
    printDate() {
      return new Date().toLocaleDateString();      
    },
    printTime () {
      return new Date().toLocaleTimeString();
    },
    printYear () {
      return new Date().getFullYear();
    },          
    printTimestamp () {
      return Date.now();
    },
    printFullDate: function(){
      return new Date();
    },
    printminutos: function(){
      return new Date().getMinutes();
    },
    printsegundos: function(){
      return new Date().getSeconds();
    },
    semillas(){            
      this.printTime(),
      this.segundos1= new Date().getMinutes();
      this.part1=(this.segundos1 % 100 - this.segundos1 % 10)/10,
      this.part2=this.segundos1 % 10,
      this.repetir= new Date().getSeconds();
      this.fibonacci=[]
      this.fibonacci[0] = this.part1
      this.fibonacci[1] = this.part2
      for (var i = 2; i < (this.repetir+1); i++) {
        this.fibonacci[i] = this.fibonacci[i - 2] + this.fibonacci[i - 1];
      }
      console.log(this.fibonacci)
      // this.fibonacci.sort((unNumero, otroNumero) => otroNumero - unNumero);
    }
  },
        mounted: function () {

          this.reloj()

          this.fecha = this.printDate();
          this.time = this.printTime();
          this.timestamp = this.printTimestamp();
          this.year = this.printYear();
          this.fulldatetime = this.printFullDate();
          
        },
  
}
  // components: {
  //   HelloWorld
  // }

</script>