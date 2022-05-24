<template>
  <div class="">
    <div class="">
      <div class="container-fluid">
        <div class="row">
          <div class="col-xl-12 text-center title-blog">
            <div>Storie di GVHD</div>
          </div>
        </div>
      </div>
    </div>
    <div class="">
      <div class="container-fluid">
        <div class="row">
          <div class="col-xl-12 text-center">
            <PostList />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import PostList from "@/components/Posts/PostList";
export default {
  components: {
    PostList,
  },
};
</script>
<style scoped>

.bg-blog {
  width: 100%;
  height: auto;
  top: 0;
  left: 0;
  background: url(/images/bg-lading-up.svg) no-repeat center top;
  position: static;
  z-index: -1;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  margin: 0 auto;
}

.title-blog{
 font-size:x-large;
 font-weight:700;
 color: white;
 padding: 1em;
}

</style>
