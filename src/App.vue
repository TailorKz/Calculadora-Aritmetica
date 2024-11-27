<script setup>
import { ref, watch } from 'vue'

const num1 = ref()
const num2 = ref()
const operador = ref('+')
const resultado = ref(0)

const calcular = () => {
  if (operador.value === '+') {
    resultado.value = num1.value + num2.value
  } else if (operador.value === '-') {
    resultado.value = num1.value - num2.value
  } else if (operador.value === 'x') {
    resultado.value = num1.value * num2.value
  } else if (operador.value === '÷') {
    resultado.value = num1.value / num2.value
  } else {
    resultado.value = 'Erro no cálculo'
  }
}
 watch([num1, num2, operador], calcular)
</script>
<template>
<div class="main">
  <h1 id="h1" class="mt-5">Calculadora aritmética</h1>
    <div class="row d-flex justify-content-center mt-5" id="input">
      <div class="col-md-2">
        <div class="input-group mb-3" id="n1">
        <input v-model="num1" type="number" class="form-control" aria-label="Sizing example input" aria-describedby="inputGroup-sizing-default" placeholder="Digite um número">
        </div>
      </div>
      <div class="col-md-1">
        <select v-model="operador" class="form-select text-center" aria-label="Default select example" id="operador">
            <option selected>Operador:</option>
            <option value="+">+</option>
            <option value="-">-</option>
            <option value="x">x</option>
            <option value="÷">÷</option>
        </select>
      </div>
      <div class="col-md-2">
        <div class="input-group mb-3" id="n2">
        <input v-model="num2" type="number" class="form-control" aria-label="Sizing example input" aria-describedby="inputGroup-sizing-default" placeholder="Digite um número">
        </div>
      </div>
  </div>
  <div class="row d-flex justify-content-center mt- ">
      <div class="col-md-4 d-flex justify-content-center mb-5">
        <div class="input-group input-group-lg" id="res">
          <span class="input-group-text" id="inputGroup-sizing-lg">=</span>
          <input :value="resultado" readonly type="number" class="form-control" aria-label="Sizing example input" aria-describedby="inputGroup-sizing-lg">
        </div>
      </div>
    </div>
</div>
  
  
</template>

<style scoped>
#h1 {
  display: flex;
  text-align: center;
  margin: 0 auto;
  justify-content: center;
  padding-top: 30px;
  
}

.main {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  border-radius: 10px; 
  background-color: rgb(235, 235, 235);
  margin-top: 6%;
}


@media (max-width: 768px) {
#operador {
  margin-bottom: 10px;
  max-width: 50%;
  margin: 0 auto 10px;
}
#n2 {
  max-width: 70%;
  margin: 0 auto;
}
#n1 {
  max-width: 70%;
  margin: 0 auto;
}
#res {
  max-width: 80%;
  margin: 0 auto;
}
}
</style>
