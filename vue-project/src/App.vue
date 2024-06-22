<script setup>
import { reactive } from 'vue';
const primeiroNUmero = document.getElementById("operacaoUm");
const segundoNUmero = document.getElementById("operacaoDois");

const estado = reactive({
  adicao: '+',
  subtracao: '-',
  divisao: '/',
  multiplicacao: '*'
})

function calculadora() {
  return primeiroNUmero, segundoNUmero;
}

calculadora();
//javascript
</script>

<template> 
<!-- html -->
<div class="container">
  <h1>Calculadora</h1>
<div>
  <p>Escolha a operação desejada</p>
    <select>
      <option value="adicao" selected>+
        {{ estado.adicao }}
      </option>
      <option value="subtracao">-
        {{ estado.subtracao }}
      </option>
      <option value="divisao">/
        {{ estado.divisao }}
      </option>
      <option value="multiplicacao">*
        {{ estado.multiplicacao }}
      </option>
    </select>
</div>
 <div id="calc">
  <input id="operacaoUm" type="number" min="1" placeholder="Digite o primeiro número">
  <span id="operador"></span>
  <input id="operacaoDois" type="number" min="0" placeholder="Digite o segundo número">
</div>
</div>

</template>

<style scoped>
</style>
