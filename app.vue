<template>
  <div>
<h1>H!</h1>
<p v-for="m in mappedItems">{{ m.text }}</p>
  </div>
</template>
<script setup>
const mappedItems=ref([
  {id:1,text:"HERE"},
  {id:2,text:"There"}
])
</script>
