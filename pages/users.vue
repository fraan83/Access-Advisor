<template>
  <div class="card">
    <div class="container-fluid" style="margin-top: 1em">
      <input type="text" v-model="userId" />
      <button @click="onloadUser" class="btn btn-sm btn-primary">
        Load User
      </button>
      <nuxt-child />
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      userId: "",
    };
  },
  methods: {
    onloadUser() {
      this.$router.push("/users/" + this.userId);
    },
  },
  layout: "users",
};
</script>
