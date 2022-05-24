<template>
  <div class="row">
    <div class="col-xl-12">
      <div class="row">
        <div class="col-lg-6">
          <PostPreview
            id="1"
            :is-admin="isAdmin"
            author="Riccardo Cascione"
            thumbnails="/images/blog/test1.jpg"
            title="Test Titlo 1 "
            previewtext="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. "
          />
        </div>
        <div class="col-lg-6">
          <PostPreview
            id="2"
            :is-admin="isAdmin"
            author="Riccardo Cascione"
            thumbnails="/images/blog/test2.jpg"
            title="Test Titlo 2 "
            previewtext="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. "
          />
        </div>
      </div>
      <div class="row">
        <div class="col-lg-6">
          <PostPreview
            id="3"
            :is-admin="isAdmin"
            author="Riccardo Cascione"
            thumbnails="/images/blog/test3.jpg"
            title="Test Titlo 3 "
            previewtext="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. "
          />
        </div>
        <div class="col-lg-6">
          <PostPreview
            id="4"
            :is-admin="isAdmin"
            author="Riccardo Cascione"
            thumbnails="/images/blog/test4.jpg"
            title="Test Titlo 4 "
            previewtext="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. "
          />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import PostPreview from "./PostPreview";
export default {
  components: {
    PostPreview,
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false,
    }
  },

  name: "PostList",
};
</script>
<style scoped>
.bg-thumbnails {
  width: 100%;
  height: 200px;
  top: 0;
  left: 0;
  background: no-repeat center top;
  position: static !important;
  z-index: -1;
  background-size: cover;
  margin: 0 auto;
  border-radius: 4px;
}
</style>
