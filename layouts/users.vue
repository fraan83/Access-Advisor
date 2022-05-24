<template>
  <div>
        <Navbar />
    <header class="card">
      Gestione Utenti
    </header>

    <nuxt />
  </div>
</template>
 <script>
 import Navbar from '@/components/Navbar.vue'
 export default {
   components: {
     Navbar
   }
 }
 </script>
<style scoped>
header{
  font-size: 1em;
  font-weight: 600;
  padding: 1em;

}
</style>
