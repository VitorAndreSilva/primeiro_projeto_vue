<script setup>
  import { computed, ref} from 'vue';

    const nome = 'Vitor'
    const idade = 16
    const contador = ref(0)

    function inverter(texto) {
        return texto.split('').reverse().join('')
    }

    function saudacao() {
        return `Olá, ${nome}!`
    }

    function incrementarContador() {
        contador.value++
        // maiorQueDez();
    }

    function decrementarContador() {
        contador.value--
        // maiorQueDez();
    }

    const maiorQueDez = computed(() => ({
      color: contador.value > 10 ? "red" : "green"
    }))

    // function maiorQueDez() {
    //   console.log(contador.value)
      
        // if (contador.value > 10) {
        //   console.log("vermelho")
        //   return {color: "red"}
        // } else {
        //   console.log("verde")
        //   return {color: "green"}
        // }
    // }

</script>

<template>
    <div class="info">
        <h1> {{ saudacao() }}  </h1>
        <h2>Informações</h2>
        <p>Nome: {{ nome }} </p>
        <p>Idade: {{ idade }}  anos</p>
        <hr />
        <h2>Mais dados:</h2>
        <p>Para completar 50 anos faltam: {{ 50 - idade }}  anos</p>
        <p>O nome tem {{ nome.length }}  caracteres</p>
        <p>O nome invertido é: {{ inverter(nome.toUpperCase()) }} </p>
        <hr />
        <p> Exemplo de saudação usando função</p>
        <p>Contador: {{ contador }}</p>
        <button @click="incrementarContador">Incrementar</button>
        <button @click="decrementarContador">Decrementar</button>
        <div :style="maiorQueDez" class="box">Box Box</div>
        <!-- <div :style="{ color: contador.value > 10 ? 'red' : 'green'}">Box box</div> -->
    </div>
</template>

<style scoped>
.info {
  background-color: rgba(35,12,22,1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}

h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}

button {
  background-color: rgba(35,12,22,1);
  color: rgb(183, 210, 219);
  border: 1px solid white;
  border-radius: 7px;
  margin-right: 0.5vw;
  cursor: pointer;
  height: 2vw;
}

button:hover {
  background-color: rgb(183, 210, 219);
  color: rgba(35,12,22,1);
}

.box {
  background-color: white;
  height: 3vw;
  margin-top: 1vw;
  border-radius: 5px;
  /* color: rgba(35,12,22,1); */
  text-align: center;
  align-content: center;
}

</style>