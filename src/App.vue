<script setup>
  import Table from './components/Table.vue';
</script>

<template>
  <div class="container">
    <div class="col-sm-7 col-sm-offset-2">
      <h1>To-Do App</h1>
      <Table />
      <Form />
    </div>
  </div>
</template>

<style scoped>
 h1 {
  color: rgb(212, 9, 9);
  text-align: center;
  padding-top: 30px;
 }
 
</style>
