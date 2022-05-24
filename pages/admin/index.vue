<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-xl-12">
        <section class="new-post">
          <div class="container rounded border m-2 alert alert-info">
            <p>
              Lo scopo di questo blog è di raccogliere le storie, le esperienze
              e i consigli di chi affronta la GVHD.
            </p>
            <p>
              Per scrivere sul blog è necessario
              <a href="#"> registrarsi al sito gvhd.it </a>
            </p>
          </div>
          <button
            class="btn btn-lg btn-success"
            @click="$router.push('/admin/new-post')"
          >
            <i class="fa-solid fa-pen"></i> Scrivi un nuovo post
          </button>
        </section>
      </div>
    </div>

    <div class="row">
      <div class="col-xl-12">
        <section class="existing-post">
          <div class="container rounded border text-center p-1">
            <h3>Ultimi post del blog</h3>
          </div>
          <PostList />
        </section>
      </div>
    </div>
  </div>
</template>

<style scoped>
.new-post {
  display: flex;
  flex-wrap: nowrap;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 2em;
}

.existing-post {
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  align-content: center;
  justify-content: center;
  align-items: center;
}

@media screen and (max-width: 800px) {
  .new-post {
    display: flex;
    flex-wrap: nowrap;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 2em;
  }
}
</style>
<script>
import PostList from "@/components/Posts/PostList";

export default {
  name: "Adminpage",
  components: {
    PostList,
  },
};
</script>
