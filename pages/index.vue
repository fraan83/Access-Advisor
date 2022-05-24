<template>
  <div>
    <div class="container-fluid" style="position: relative">
      <div class="row ">
        <div class="col-xl-12">
          <div class="row">
            <div class="col-xl-12">
              <div class="" style="margin-top: 0.5rem">
                <h2>Benvenuti sul blog di GVHD Italia</h2>
                <h5>
                  Qui troverai risorse utili in italiano sulla malattia del
                  trapianto contro l'ospite.
                </h5>
              </div>
            </div>
          </div>
          <div class="row">
            <div class="col-xl-12">
              <h6 class="sectionTitle">Le ultime dal blog</h6>
            </div>
          </div>
          <div class="row">
            <PostList />
          </div>

          <div class="row" style="margin: 0.75rem">
            <div class="col-xl-12">
              <div class="container-fluid text-center">
                <nuxt-link to="/posts/">
                  <button class="btn btn-lg btn-pink"> <i class="fa-solid fa-book-open-reader"></i> Leggi i post dei lettori </button>
                </nuxt-link>
              </div>
            </div>
          </div>

          <div class="row">
            <div class="col-xl-12">
              <h6 class="sectionTitle">Aggiornamenti dalla ricerca</h6>
            </div>
          </div>
          <div class="row">
          <NewsList />
          </div>
        </div>
      </div>

    </div>

  </div>
</template>
<style scoped>
.bg-landing {
  width: 100%;
  height: auto;
  top: 0;
  left: 0;
  background: url(/images/bg-lading-up.svg) no-repeat center top;
  position: absolute;
  z-index: -1;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  margin: 0 auto;
}
h2 {
  color: white;
}
h5 {
  color: white;
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
import PostList from "@/components/Posts/PostList.vue";
import PostPreview from "@/components/Posts/PostPreview.vue";
import NewsPreview from "@/components/News/NewsPreview.vue";
import NewsList from "@/components/News/NewsList.vue";
import Footer from "@/components/sections/Footer.vue";
export default {
  components: {
    PostPreview,
    NewsPreview,
    PostList,
    NewsList,
  },
  name: "Home",
  layout: "default",
};
</script>
