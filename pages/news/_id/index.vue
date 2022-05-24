<template>
  <div>
    <div class="container-fluid">
      <div class="row">
        <div class="col-xl-12">
          <h2>Titolo del post</h2>
        </div>
      </div>
      <div class="row rounded border">
        <div class="col-sm-6">
          <div>pubblicato il <b>10/10/22</b></div>
        </div>
         <div class="col-sm-6 justify-content-end text-right" style="text-align: end;">
            <div>da <b><i>Autore</i></b></div>
        </div>
      </div>
      <div class="row">
         <div class="col-xl-4">
          <img
            class="img-fluid"
            src="/images/microscope.svg"
            alt="immagine post"
          />
        </div>
        <div class="col-xl-8">
          <p style="font-weight: 400;">
            Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod
            tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim
            veniam, quis nostrum exercitationem ullam corporis suscipit
            laboriosam, nisi ut aliquid ex ea commodi consequatur. Quis aute
            iure reprehenderit in voluptate velit esse cillum dolore eu fugiat
            nulla pariatur. Excepteur sint obcaecat cupiditat non proident, sunt
            in culpa qui officia deserunt mollit anim id est laborum.
          </p>
        </div>

      </div>
      <div class="row">
        <div class="col-xl">
          <div class="btn-group" role="group" aria-label="Basic example">
            <button type="button" class="btn btn-primary">
              <i class="fa-brands fa-facebook-square"></i>
            </button>
            <button type="button" class="btn btn-primary">
              <i class="fa-brands fa-twitter-square"></i>
            </button>
            <button type="button" class="btn btn-primary">
              <i class="fa-brands fa-linkedin"></i>
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

 <script>
 import style from "../news.css"
 export default {

 }
 </script>
