<template>

  <section class="src-components-final">
    <div>
        <Primeropunto />
        <br>
        <Respuestas />
    </div>
  </section>

</template>

<script>

import Primeropunto from './Primeropunto.vue'
import Respuestas from './Respuestas.vue'

export default  {
    name: 'src-components-final',
    props: [],
    components: {
      Primeropunto,
      Respuestas
    },
    mounted () {

    },
    data () {
      return {

      }
    },
    methods: {

    },
    computed: {

    }
}


</script>

<style scoped lang="css">
  .src-components-final {

  }

  .text-lightblue {
    color: lightblue;
  }
</style>
