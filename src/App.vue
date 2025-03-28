<script setup>
  import { ref } from 'vue'
    let id = 0
  //variable
  const msg = ref('Tuto vue.js  ')
  const newItem = ref('')
  const items = ref([
    { id: id++, name: 'item 1' },
    { id: id++, name: 'item 2' },
    { id: id++, name: 'item 3' },
    { id: id++, name: 'item 4' },
    { id: id++, name: 'item 5' },
  ])
  // function
  const addItem = () => {
    items.value.push({ id: id++, name: newItem.value })
    newItem.value = ''
  }
  const deleteItem = (id) => {
    items.value = items.value.filter(item => item.id !== id)
  }

</script>

<template>


  <main id="main">
        <h1 >{{ msg }}</h1>
       <ul>
        <li v-for="item in items" :key="item.id">
          {{ item.name }}
          <button @click="deleteItem(item.id)">X</button>
        </li>
     
       </ul>
       <input type="text" v-model="newItem">
       <button @click="addItem">Ajouter</button>
    
  </main>
</template>

<style scoped>

</style>
