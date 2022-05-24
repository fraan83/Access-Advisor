<template>
  <div>
    <div class="container-fluid">
      <div class="row">
        <div class="col-xl-12">
          <div class="title_blog">Titolo del post</div>
        </div>
      </div>
      <div class="row rounded border p-1 m-3">
        <div class="col-sm-6">
          <div>pubblicato il <b>10/10/22</b></div>
        </div>
        <div
          class="col-sm-6 justify-content-end text-right"
          style="text-align: end"
        >
          <div>
            da <b><i>Autore</i></b>
          </div>
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
          <p style="font-weight: 400">
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
      <div class="row">
        <div class="col-xl-12">
          <div class="sectionTitle">
            Post correlati
          </div>
            <PostList />
        </div>

      </div>
    </div>

  </div>

</template>

<style scoped>
.title_blog {
  color: white;
  text-shadow: -0.5px -0.5px 2px rgba(150, 150, 150, 1);
  font-size: xx-large;
  font-weight:800;
}
.sectionTitle {
  font-size: 1.1em;
  font-weight: 600;
  color: rgb(255, 255, 255);
  background-color: #2988c0;
  padding: 0.5rem;
  border-radius: 4px;
  margin-top: 1em;
  padding: 0.75em;
}
</style>

<script>
import style from "../post.css";
import PostList from "@/components/Posts/PostList.vue";
export default {
name:"Post",
components:{
  PostList,
}
};
</script>
