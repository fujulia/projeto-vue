<script setup>
import { ref } from 'vue';
const contador = ref(0);

function incrementarContador(){
  contador.value++
}

function decrementarContador(){
  if(contador.value>0){
    contador.value--;
  }
}

function zerarContador(){
  contador.value = 0;
}

/*let nome= "Eduardo"
const pessoa= {
  nome: "Eduardo",
  cidade: "São Paulo"
}
pessoa.nome="nova.pessoa"*/

</script>

<template>
  <button @click="incrementarContador()">+</button>
  <button @click="decrementarContador()">-</button>
  <button @click="zerarContador()">Zerar</button>

 <p>Valor do contador: {{ contador }}</p>
</template>

<style scoped>
  
  button {
  font-weight: bold;

}

</style>
