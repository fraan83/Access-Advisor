<template>
  <div class="row">
    <div class="col-xl-12">
      <div class="new-post-form">
        <form style="width: 100%" @submit.prevent="onSave">
          <AppControlInput v-model="editedPost.author">
            <label>Nome Autore: </label>
          </AppControlInput>

          <AppControlInput v-model="editedPost.title">
            <label>Titolo: </label>
          </AppControlInput>

          <AppControlInput v-model="editedPost.thumbnailLink">
            <label>Immagine: </label>
          </AppControlInput>

          <AppControlInput control-type="textarea" v-model="editedPost.content">
            <label>Corpo del testo:</label>
          </AppControlInput>
          <div class="container text-center containerPulsanti">
            <AppButton btn-style="btn-sm btn-success" type="submit">
              <i class="fa-solid fa-circle-check"></i> Salva
            </AppButton>

            <AppButton
              type="button"
              style="margin-left: 10px"
              btn-style="btn-sm btn-danger"
              @click="onCancel"
              ><i class="fa-solid fa-circle-minus"></i> Cancella
            </AppButton>
          </div>
        </form>
      </div>
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

.containerPulsanti {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  align-content: center;
  flex-wrap: nowrap;
  flex-direction: row;
  margin-bottom: 10px;
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
export default {
  name: "AdminPostForm",
  components: {
    AppControlInput,
    AppButton,
  },
  props: {
    post: {
      type: Object,
      required: false,
    },
  },
  data() {
    return {
      editedPost: this.post
        ? { ...this.post }
        : {
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
