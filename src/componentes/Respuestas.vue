<template>

  <section class="src-components-respuestas">
      <div>
      <h2>Respuestas</h2>
      <br>

      <div class="table-responsive">
        <table class="table">
          <tr>
            <th>Pregunta</th>
            <th>Respuesta</th>
          </tr>
           <tr v-for="(pregunta,index) in preguntas" :key="index" >
            <td>{{ pregunta.numero }}</td>
            <td>{{ obtenerRespuesta(pregunta.respuestas) }}</td>
          </tr>
        </table>
      </div>       

    </div>
  </section>

</template>

<script>

  export default  {
    name: 'src-components-respuestas',
    props: [],
    mounted () {

    },
    data () {
      return {
        preguntas : [
          { numero: 1, respuestas: ['b'] },
          { numero: 2, respuestas: ['c'] },
          { numero: 3, respuestas: ['b'] },
          { numero: 4, respuestas: ['d'] },
          { numero: 5, respuestas: ['d'] },
        ]
      }
    },
    methods: {
      obtenerRespuesta(respuestas){
        let respuestaConcatenada = ''
        respuestas.forEach(respuesta => {
          respuestaConcatenada += respuesta + ', '
        });
        if(respuestaConcatenada.endsWith(', ')) 
          respuestaConcatenada = respuestaConcatenada.substring(0, respuestaConcatenada.length - 2)

        return respuestaConcatenada
      }
    },
    computed: {

    }
}


</script>

<style scoped lang="css">
  .src-components-respuestas {

  }
</style>
