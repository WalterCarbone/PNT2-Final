<template>

  <section class="src-components-formulario">
    <h1>Final NT 2</h1>
    <label for="Color">Color </label>   
    <input type="text" v-model="color"> <br>

    <label for="Fondo">Fondo </label> 
    <input type="text" v-model="fondo" > <br>

    <label for="Size">Size</label> 
    <input type="text" v-model="size" > <br>

    <hr>
    <label for="texto">Texto</label>   
     <input type="text" v-model="texto"  :style="getEstilos()" > <br>

    <hr>
    <p>cantidad de palabras: {{contarPalabras}} </p>

        <h2>Respuestas:</h2>
    <p>1:b , 2:c, 3:b, 4:a , 5:d</p> 
  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-components-formulario',
    props: [],
    mounted () {

    },
    data () {
      return {
        texto:'',
        color:'',
        fondo:'',
        size:'',
      }
    },
    methods: {
        actualizar(){
          
        },

    getEstilos() {
          return { 
              color:this.color, 
              backgroundColor:this.fondo, 
              fontSize:this.size,              
          }
      }    
    },
    computed: {
         contarPalabras(){         
         var cant=this.texto.split(' ').length
         
         return cant
         
        }
    }
}


</script>

<style scoped lang="css">
  .src-components-formulario {

  }
</style>
