<template>

  <section class="src-componentes-primer-punto">
    <h3>Primer punto</h3>
      <hr>
      <p>Color: <input label type="text" v-model="color" name="color"></p>
      <p>Fondo: <input type="text" v-model="fondo" name="fondo"> </p>
      <p>Size: <input type="text" v-model="size" name="size"> </p>

      <br>
      

      <p>Texto: <input label type="text" v-model.trim="texto" :style="getClass()" name="texto"></p>

      <span>
          Cantidad de palabras: {{ calcularCantidadPalabras }}
      </span>


  </section>

</template>

<script>

  export default  {
    name: 'src-componentes-primer-punto',
    props: [],
    mounted () {

    },
    data () {
      return {
        color : '',
        fondo: '',
        size: '',
        texto: ''
      }
    },
    methods: {
      getClass(){
        let classTexto = ''
        if(this.fondo != '')
          classTexto += 'background-color: ' + this.fondo + ';'

        if(this.color != '')
          classTexto += 'color: ' + this.color + ';'

        if(this.size != '')
          classTexto += 'font-size: ' + this.size + ';'

        console.log(classTexto)
        return classTexto
      }
    },
    computed: {
        calcularCantidadPalabras() {
            let cantidadPalabras;
            if(this.texto.trim() == '')
              cantidadPalabras = 0
            else
              cantidadPalabras = this.texto.trim().split(' ').length

            return cantidadPalabras
        }
    }
}


</script>

<style scoped lang="css">
  .src-componentes-primer-punto {

  }
</style>
