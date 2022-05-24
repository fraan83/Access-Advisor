<template>
<div class="container-fluid">
  <div class="text-center errorContainer">
   <img class="errorImage" src="/images/warning.gif" alt="error" />
    <h1> Siamo spiacenti, ma la risorsa richiesta non è disponibile. </h1>
  </div>

</div>

</template>
<style scoped>
  .errorContainer{
    display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
    justify-content: center;
    align-items: center;
    align-content: center;
    max-width: 512px;
    margin: 0 auto;
  }
  .errorImage{
    max-width: 312px;
  }
</style>
