<script setup>
  import { ref, onMounted } from 'vue'

const contador = ref(0)

function incrementarContador() {
  contador.value++
}
function decrementarContador() {
  if(contador.value > 0){
    contador. value--
  }
}
function reiniciar(){
  contador.value = 0
}
onMounted(() => {
  console.log(`O valor inicial do contador é ${contador.value}.`)
})
</script>

<template>
  <div class="container">
    '<button @click="incrementarContador">Incrementar</button>
  <button @click="decrementarContador">Decrementar</button>
  <button @click="reiniciar">Zerar contador</button>
  <p>Valor do contador é: {{ contador }}</p>'
  </div>
</template>

<style>

  button {
  width: 100px;
  height: 30px;
  font-weight:bolder;
  border-radius: 20px;
  border: 3px solid rgb(247, 93, 175);
  background-color: rgb(247, 106, 181);
}
body{
  background-color: black;
}
p{
  color: aliceblue;
}
.container{
  display: grid;
  grid-template-columns: auto;
  
}
</style>
