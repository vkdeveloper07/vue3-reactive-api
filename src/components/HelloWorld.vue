<script setup>
import { reactive } from 'vue';

const state = reactive({data:'testing', number:20})

function changeData(){
  state.data = 'changed data';
}

function changeNumber(){
  state.number = 30;
}
</script>

<template>
  <div class="container">
   <p>Reactive state object's data</p>
   <p> {{ state.data }}</p>
   <p> {{ state.number }}</p>
   <button class="btnData" @click="changeData">Change Data</button>
   <button class="btnData" @click="changeNumber">Change Number</button>
  </div>
</template>

<style scoped>
.container{
  width:100%;
  border: 2px solid white;
}
.btnData{
  margin: 10px;
  width: 150px;
  height: 30px;
  border: 1ps solid black;
  border-radius: 8px;
}
</style>
