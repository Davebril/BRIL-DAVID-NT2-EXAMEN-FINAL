<template >

  <section class="src-componentes-conversor">
    <h1>Conversor de temperatura</h1>

    <span>Ingrese temperatura °C </span>  <input type="number" v-model="tempCelsius"> <br>
    <br>
    
    <br><br>

    <span>Conversión a °F </span> <span  :style="{color: SeleccionColor(this.tempCelsius).color }"> 
    {{tempF = tempCelsius * constMultiplicada + constSumada}} </span> <br> 
    <br>

    <span>Conversión a °K </span> <span  :style="{color: SeleccionColor(this.tempCelsius).color }"> 
    {{tempK = tempCelsius * 1 + enKelvin}} </span> <br> 
    <br> 
    

         <br>

      <h4> Respuestas a las preguntas </h4>

      <p> Respuestas:  1:c</p>
      <p> Respuestas:  2:b</p>
      <p> Respuestas:  3:c</p>
      <p> Respuestas:  4:a</p>
      <p> Respuestas:  5:c</p>

  </section>

</template>

<script>

  export default  {
    name: 'src-componentes-conversor',
    props: [],
    mounted () {


    },






    data () {
      return {
        // TEMPERATURA KELVIN SACADA DE GOOGLE

        tempCelsius:null,
        enKelvin: 273.15, 
        constMultiplicada: 1.8,
        constSumada: 32

      }
    },
    methods: {


      SeleccionColor(temperatura) {
        let color = '#magenta'
        if(temperatura < 0) color = '#0000ff'
        else if(temperatura >= 0 && temperatura < 15) color = '#d000ff'
        else if (temperatura >= 15) color = '#ff0000'
        return {
          color
        }
      },

    },
    computed: {

      

    }
}


</script>

<style scoped lang="css">
  .src-componentes-conversor {
    
  }
</style>