<!-- <script setup>
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

</script> -->

<script>
export default{
  data(){
    return{
      contador:0
    }
  }, 
  methods:{
    incrementarContador(){
      this.contador++
    },
    decrementarContador(){
      if(this.contador>0){
        this.contador--
      }
    },
    zerarContador(){
      this.contador = 0
    }
  },
  mounted(){
    console.log(`O valor inicial do contador é ${this.contador}.`)
  }
}


</script>

<template>
  <div id="contadorBloco">
  <p>Valor do contador: {{ contador }}</p>
  <div id="buttonsValores">
    <button id="buttonVerde" @click="incrementarContador()">+</button>
    <button id="buttonVermelho" @click="decrementarContador()">-</button>
  </div>
 
  <button id="buttonZerar" @click="zerarContador()">Zerar</button>


</div>
</template>

<style scoped>

  
  button {
  font-weight: bold;
  border: none;
}
  p{
    text-align: center;
    font-size: 18px;
  }

  #contadorBloco{
    border: 1px solid rgb(170, 198, 230);
    width: 300px;
    margin: auto;
    background-color: rgb(203, 225, 231);
  }

  div #buttonsValores{
    width: 80px;
    margin: auto;
  }

  #buttonsValores button{
    border-radius: 50%;
    width: 30px;
    height: 30px;
    margin: 5px;
  }

  #buttonZerar{
    width: 50%;
    left: 24%;
    position: relative;
    margin: 5px;
    text-align: center;
    font-size: 16px;
  }

  #buttonZerar button{
    text-align: center;
  }

  #buttonZerar:hover {
    background-color: red; 
    transition: 0.4s;
    opacity: 0.7;
    color: white;
}

  #buttonVerde{
    background-color: rgb(79, 216, 45);
  }

  #buttonVerde:hover, #buttonVermelho:hover{
    opacity: 0.7;
  }

  #buttonVermelho{
    background-color: rgb(255, 113, 113);
  }

</style>
