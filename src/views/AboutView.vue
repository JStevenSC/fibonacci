<template>
  <div class="about">

    <b-row class=" d-flex   flex-row">

      <b-col md="7" class=" d-flex text-center  flex-column">
        <img alt="logoe" src="../assets/logo.png" class="img-fluid" >
      </b-col>
      
      <b-col md="5" class=" d-flex text-center  flex-column">
       
        <h2 class="text-center mb-3">Serie de fibonacci usando Hora actual</h2>
        
            <button  @click="semillas()">Calcular</button>
            
            <h1> {{ mostrar}}</h1>
            <h4> {{ 'semilla1=' }} {{ part1}}</h4>
            <h4> {{ 'semilla2=' }} {{ part2}}</h4>
            <h4> {{ 'Repetir=' }} {{ repetir}}</h4>
            <h4> {{ fibonacci }} </h4>

      </b-col>
    </b-row>
  </div>
</template>


<script>
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
      fibonaccidesc: [],
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
      this.fibonaccidesc=[]
      this.fibonacci[0] = this.part1
      this.fibonacci[1] = this.part2
      for (var i = 2; i < (this.repetir+1); i++) {
        this.fibonacci[i] = this.fibonacci[i - 2] + this.fibonacci[i - 1];
      }
      console.log(this.fibonacci)  
 
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

</script>

<style>

.about{
  background-image: url("../assets/fondo3.png");  
}
.texto{
  text-align: justify;
}

</style>