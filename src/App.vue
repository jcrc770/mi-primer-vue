<script setup>
  const name = 'Vue dinámico'
  const styleColor = 'color: blue'
  const arrayColores = ['blue', 'red', 'peru']
  const activo = true
</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <h2>{{ arrayColores }}</h2>
  <h2 :style="`color: ${arrayColores[2]}`">Soy Peru</h2>

  <h2>{{ activo ? 'Estoy activo' : 'Estoy Inactivo' }}</h2>

  <!-- Directivas -->
   <!-- v-if -->
    <p v-if="activo === true">Estoy activo</p>
    <p v-else-if="activo === false">Estoy Inactivo</p>
    <p v-else="activo">Estoy Indeciso</p>
</template>

<style scoped>
 h1{
  color: red;
 }
</style>