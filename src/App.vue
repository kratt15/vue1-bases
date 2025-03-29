<script setup>
  import { ref, computed } from 'vue'
    let id = 0
  //variable
  const msg = ref('Tuto vue.js 2025')
  const fName = ref('Sidney')
  const lName = ref('Consti')

  const fullname = computed(() => {
    return fName.value + " " + lName.value.toUpperCase()
  })
 

</script>

<template>


  <main id="main">
        <h1 >{{ msg }}</h1>
        <h2>Bonjour  {{ fullname }}</h2>
    
  </main>
</template>

<style scoped>

</style>
