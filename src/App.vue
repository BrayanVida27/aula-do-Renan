<script setup lang="ts">
const escola = 'Senai'
const cidade = 'Tubarão'
let nome = 'Brayan'
let idade = 18
let filme1 = 'jogador número 1'
let filme2 = 'five nights at freddy s'
let filme3 = 'minecraft'

function desabilitado(){
  return idade < 18;
}

function mostraAlert(){
  alert('Clicou no botão')
}

function mudouSelect(event: Event){
  alert((event.target as HTMLSelectElement).value)
}
</script>

<template>
  <div class="container">
    <div class="row">
    <div class="col">
      <button @click="mostraAlert" :disabled="desabilitado()" class="btn btn-primery">Habilitado</button>
      <select @change="mudouSelect($event)" class="form-select" name="teste" id="teste">
        <option>valor 1</option>
        <option>valor 2</option>
        <option>valor 3</option>
      </select>
   <h1>Ola mundo projeto vue</h1>
   <p>Escola é {{ escola }} da cidade {{ cidade }} </p>
   <H1> sou {{ nome }}, e tenho {{ idade }} anos</H1>
   <ol>
    <li>{{ filme3.toLowerCase() }}</li>
    <li>{{ filme1.toLowerCase() }}</li>
    <li>{{ filme2.toLowerCase() }}</li>

   </ol>
    </div>
   </div>
  </div>
</template>

<style>
h1{
  color: rgb(73, 65, 175);
}

p{
  font-size: 30PX;
}
</style>