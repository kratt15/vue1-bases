<script setup>
  import { ref } from 'vue'

  //variable
  const msg = ref('Tuto vue.js  ')
 const jour= ref(true)
  // function
  const changer =()=>{
    jour.value = !jour.value
  }
</script>

<template>


  <main id="main" :class="jour ? 'jour' : 'nuit'">
        <h1 >{{ msg }}</h1>
        <h2 v-show="jour">Jour</h2>
        <h2 v-show="!jour">Nuit</h2>

        <button @click="changer">Changer</button>
    
  </main>
</template>

<style scoped>
#main{
  background-color: #94ddf3;
  position: absolute;
  top:0;
  left:0;
  right:0;
  bottom:0;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.nuit{
  background-color: #11233d !important;
  position: absolute;
  top:0;
  left:0;
  right:0;
  bottom:0;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  color: #fff;
}

</style>
