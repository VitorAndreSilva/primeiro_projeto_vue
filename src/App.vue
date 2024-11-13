<script>
// Lógica do componente / JavaScript //
export default {
  data() {
    return {
      contador: 0
    }
  },
  methods: {
    incrementarContador() {
      this.contador++
    },
    decrementarContador(){
      this.contador--
    }
  },
  mounted() {
    console.log(` valor inicial do contador é ${this.contador}`)
  }
}
</script>
<template>
  <!-- Template do componente / HTML5 -->

  <button @click="incrementarContador">Incrementar</button>
  <button @click="decrementarContador">Decrementar</button>
  <p>O valor do contador é: {{ contador }}</p>
</template>
<style scoped>
/* Estilização do componente / CSS3 */

button {
  font-weight: bold;
  background-color: greenyellow;
  height: 3vw;
  width: auto;
  border-radius: 2vw;
  margin-left: 0.5vw;
  margin-right: 0.5vw;
}

button:hover {
  background-color: green;
  color: white;
}

p {
  font-size: 1.5rem;
  font-family: 'Times New Roman', Times, serif;
  margin: 1vw 0 0 2vw;
}

</style>
