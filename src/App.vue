<script setup>

</script>

<template>
  <h1 id="h1" class="mt-5">Calculadora aritmética</h1>

  <div class="row d-flex justify-content-center mt-5">
    <div class="col-md-2">
      <div class="input-group mb-3">
      <input type="number" class="form-control" aria-label="Sizing example input" aria-describedby="inputGroup-sizing-default" placeholder="Digite um número">
      </div>
    </div>
    <div class="col-md-1">
      <select class="form-select text-center" aria-label="Default select example">
          <option selected>Operador:</option>
          <option value="1">+</option>
          <option value="2">-</option>
          <option value="3">x</option>
          <option value="4">÷</option>
      </select>
    </div>
    <div class="col-md-2">
      <div class="input-group mb-3">
      <input type="number" class="form-control" aria-label="Sizing example input" aria-describedby="inputGroup-sizing-default" placeholder="Digite um número">
      </div>
    </div>
    
</div>
<div class="row d-flex justify-content-center mt-3">
    <div class="col-md-3 d-flex justify-content-center">
      <div class="input-group input-group-lg">
        <span class="input-group-text" id="inputGroup-sizing-lg">Resultado:</span>
        <input type="number" class="form-control" aria-label="Sizing example input" aria-describedby="inputGroup-sizing-lg">
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
}
</style>
