<template>
  <div>
    more details user  id : {{ $route.params.id }}
  </div>
</template>
 <script>
 export default {
   validate (data) {
     //validazione solo valori numerici per params.id
     return /^\d+$/.test(data.params.id)
   },
   layout: 'users'
 }
 </script>
