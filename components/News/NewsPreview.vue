<template>
  <article>
    <div class="container-fluid">
      <div class="row">
        <div class="col-sm-12">
          <div class="newstitle">
            <nuxt-link
              :to="'/news/' + id"
              class="nav-item"
              style="outline: none; text-decoration: none"
            >
              <h4>{{ title }}</h4>
            </nuxt-link>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-sm-4 text-center">
          <nuxt-link
            :to="'/news/' + id"
            class="nav-item"
            style="outline: none; text-decoration: none"
          >
            <div
              class="img-fluid bg-thumbnails"
              :style="{ backgroundImage: 'url(' + thumbnails + ')' }"
            ></div>
          </nuxt-link>
        </div>
        <div class="col-sm-8">
          <div class="row">
            <div class="col-xl-12">
              <b
                ><i>{{ author }}</i></b
              >
              <small>del {{ datetime }}</small>
            </div>
          </div>
          <div class="row">
            <p>
              {{ previewtext }}
            </p>
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
}

.newstitle {
  padding: 1em;
  border-bottom: 0.5px solid #adb5bd;
  color: #185c85;
  font-weight: 900;
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
      require: true,
    },
    author: {
      type: String,
      require: true,
    },
    datetime: {
      type: String,
      require: true,
    },
    thumbnails: {
      type: String,
      require: true,
    },
  },
};
</script>
