<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-xl-12">
        <section class="update-form">
          <AdminPostForm :post="loadedPost"/>
        </section>
      </div>
    </div>
  </div>
</template>
<script>
import AdminPostForm from "@/components/Admin/AdminPostForm.vue";
export default {
  name: "postId",
  components: {
    AdminPostForm,
  },
  data() {
    return {
      loadedPost: {
        autor: 'Gianluca Caascione',
        title: 'Il Mio primo Post',
        thumbnailLink: 'images/blog/investigation.png',
        content: 'Lorem ipsum'
      }
    }
  }
};
</script>
