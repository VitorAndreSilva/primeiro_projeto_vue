<script setup>
// Lógica do componente / JavaScript //

  const numero = 1;
  const ok = true;
  const palavra = 'programar';
  function inverter(texto) {
    return texto.split('').reverse().join('');
  }

</script>
<template>
  <!-- Template do componente / HTML5 -->
  <p>{{ numero + 1 }}</p>
  <p>{{ ok ? 'Sim' : 'Não' }}</p>
  <p>{{ inverter(palavra) }}</p>

</template>
<style scoped>


</style>
