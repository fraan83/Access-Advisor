<template>
<footer>
  <div class="container-fluid">
    <div class="row">
      <div class="col-xl-12">
        <div class="footer">
          Questo Blog vuole essere un punto di incontro per persone affette
          dalla malattia del trapianto contro l'ospite, o comunemente chiamata
          (GVHD). <br />
          <strong>Attenzione!</strong> Non vi sarano <b>mai</b> chieste password
          o dati sensibili da questo sito. Questo portale non è a scopo di
          lucro.
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-xl-12">
        <div class="creditsfooter">©2022 - {{ulitmoanno}} Francesco Greco.</div>
      </div>
    </div>
  </div>
</footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      ulitmoanno: function () {
        var anno;
        var dataoggi = new Date();
        anno = dataoggi.getFullYear();
        return anno;
      },
    };
  },
};
</script>

<style></style>

<style scoped>
.footer {
  font-size: small;
}
.creditsfooter {
  text-align: center;
}
</style>
