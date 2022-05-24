<template>
  <div>
    <div class="container-fluid">
      <div class="row">
        <div class="col-xl-12">Utente con id: {{ $route.params.id }}</div>
      </div>
    </div>
  </div>
</template>

 <script>
export default {
  validate(data) {
    //validazione solo valori numerici per params.id
    return /^\d+$/.test(data.params.id);
  },
  layout: "users",
};
</script>
