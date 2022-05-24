<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-xl-12 raunded border">
        <div class="new-post-title">Nuovo post:</div>
      </div>
    </div>
    <div class="row">
      <AdminPostForm />
    </div>
    <div class="row">
      <div class="col-xl-12"></div>
    </div>
  </div>
</template>

<style scoped>
.new-post-title {
  font-size: medium;
  font-weight: 500;
  padding: 0.6em;
}
.new-post-form {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  align-content: stretch;
  justify-content: center;
  align-items: center;
  line-height: 28px;
}

label {
  font-size: small;
  text-transform: uppercase;
  font-weight: 600;
}
</style>

<script>
import AppControlInput from "@/components/UI/AppControlInput.vue";
import AppButton from "@/components/UI/AppButton.vue";
import AdminPostForm from "@/components/Admin/AdminPostForm.vue";
export default {
  name: "NewPost",
  components: {
    AppControlInput,
    AppButton,
    AdminPostForm,
  },
  data() {
    return {
      editedPost: {
        author: "",
        title: "",
        thumbnailLink: "",
        content: "",
      },
    };
  },

  methods: {
    onSave() {
      //SAVE THEPOST
    },
    onCancel() {
      //navigateback
      this.$router.push("/admin");
    },
  },
};
</script>
