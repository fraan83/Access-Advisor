<template>
  <div class="row">
    <div class="col-xl-12">
      <div class="row">
        <div class="col-lg-6">
          <NewsPreview
            id="1"
            author="Gian Nicola"
            datetime="02/02/2020"
            thumbnails="/images/blog/test4.jpg"
            title="Test Titlo 1 "
            previewtext="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. "
          />
        </div>
        <div class="col-lg-6">
          <NewsPreview
            id="1"
            author="Gian Nicola"
            datetime="02/02/2020"
            thumbnails="/images/blog/test4.jpg"
            title="Test Titlo 2 "
            previewtext="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. "
          />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import NewsPreview from "./NewsPreview";
export default ({
  components: {
    NewsPreview,
  },
   name: "PostList",
})
</script>
<style scoped>
.bg-thumbnails {
    width: 100%;
    height: 200px;
    top: 0;
    left: 0;
    background: no-repeat center top;
    position: static!important;
    z-index: -1;
    background-size: cover;
    margin: 0 auto;
    border-radius: 4px;
}
</style>
