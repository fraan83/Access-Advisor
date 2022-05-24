<template>
  <article style="margin-top: 0.5em">
    <div class="container">
      <div class="row">
        <div class="col-sm-4 text-center">
          <nuxt-link
            :to="postLink"
            style="outline: none; text-decoration: none"
          >
            <div
              class="img-fluid bg-thumbnails"
              :style="{ backgroundImage: 'url(' + thumbnails + ')' }"
            ></div>
          </nuxt-link>
        </div>

        <div class="col-sm-8">
          <div class="newstitle">
            <nuxt-link
              :to="postLink"
              class="nav-item"
              style="outline: none; text-decoration: none"
            >
              <strong> {{ title }}</strong></nuxt-link
            >
            <div>
              <small
                >di <i>{{ author }}</i></small
              >
            </div>
          </div>

          <div class="postpreview">
            {{ previewtext }}
          </div>
          <div class="buttonpost">
            <nuxt-link :to="postLink" class="btn btn-sm btn-primary">
              <i class="fa-solid fa-book-open-cover"></i> Leggi il post
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </article>
</template>
<style scoped>
.img-size {
  max-width: 80%;
  margin: 0 auto;
}
.bg-thumbnails {
  width: 100%;
  height: 200px;
  top: 0;
  left: 0;
  background: no-repeat center top;
  position: inherit;
  z-index: -1;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  margin: 0 auto;
  border-radius: 4px;
  border: 1px solid rgb(158, 158, 158);
}
.newstitle {
  padding: 1em;
  border-bottom: 0.5px solid #adb5bd;
  color: #185c85;
  font-weight: 900;
}
.postpreview {
  font-size: small;
}
.buttonpost {
  padding: 0.75em;
  border-bottom: 1px solid rgb(164, 164, 164);
  margin-bottom: 1em;
}
</style>
<script>
export default {
  name: "PostPreview",
  props: {
    id: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    previewtext: {
      type: String,
      required: true,
    },
    author: {
      type: String,
      required: true,
    },
    thumbnails: {
      type: String,
      required: true,
    },
    isAdmin: {
      type: Boolean,
      required: true,
    },

  },
  computed: {
    postLink() {
      return this.isAdmin ? '/admin/' + this.id : '/posts/' + this.id
    }
  }
};
</script>
