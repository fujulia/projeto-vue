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
    <button @click="incrementarContador()">+</button>
    <button @click="decrementarContador()">-</button>
  </div>
 
  <button id="buttonZerar" @click="zerarContador()">Zerar</button>


</div>
</template>

<style scoped>
  
  button {
  font-weight: bold;
  
}
  p{
    text-align: center;
    font-size: 18px;
  }

  #contadorBloco{
    border: 1px solid;
    width: 300px;
    margin: auto;
  }

  div #buttonsValores{
    width: 80px;
    border: 1px solid;
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
    font-size: 15px;
  }

  #buttonZerar button{
    text-align: center;
  }



</style>
