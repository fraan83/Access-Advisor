<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-light bg-azzurro">
      <div class="container-fluid">
        <a class="navbar-brand" href="/"
          ><img
            src="/images/microscope.svg"
            width="50px"
            alt="GVHDItalia logo"
          />
          GVHD Italia</a
        >

        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <div
          class="collapse navbar-collapse justify-content-end"
          id="navbarSupportedContent"
        >
          <ul class="navbar-nav me-auto mb-2 mb-lg-0 navbarMobile">
            <li class="nav-item">
              <nuxt-link class="nav-link" to="/"> Home </nuxt-link>
            </li>
            <li class="nav-item">
              <nuxt-link class="nav-link" to="/posts/"> Blog </nuxt-link>
            </li>

            <li class="nav-item">
              <nuxt-link class="nav-link" to="/about/"> Info </nuxt-link>
            </li>
            <li class="nav-item">
              <button class="btn btn-info btn-sm">
                <nuxt-link class="nav-link" to="/author/">
                  <i class="fa-solid fa-feather"></i> Raccontaci la tua storia
                </nuxt-link>
              </button>
            </li>
            <li>
              <button
                v-if="this.isLogin"

                class="btn btn-sm btn-light"
              >
                <nuxt-link class="nav-link" to="/author/">
                  {{ username }}
                </nuxt-link>
              </button>
              <button
                v-if="!this.isLogin"
                @click="this.isLogin = !isLogin"
                class="btn btn-sm btn-primary"
              >
                <nuxt-link class="nav-link" to="/author/">  Accedi </nuxt-link>
              </button>
            </li>
          </ul>
          <ul class="navbar-nav me-auto mb-2 mb-lg-0"></ul>
        </div>
      </div>
    </nav>
  </div>
</template>


<style scoped>
.bg-azzurro {
  background-color: #54c6f8 !important ;
}
.nav-link {
  font-weight: 800 !important;
}
.navbarMobile {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  align-content: stretch;
  align-items: center;
  justify-content: space-around;
}
</style>
<script>
import AppButton from "@/components/UI/AppButton.vue";

export default {
  name: "Navbar",
    layout: "default",
  components: {
    AppButton,
  },

  data() {
    return {
      isLogin: true,
      username: "Francesco",
    };
  },

  // `mounted` is a lifecycle hook which we will explain later
  mounted() {
    // `this` refers to the component instance.
    console.log(this.username) // => 1

    // data can be mutated as well
    this.username = "Francesco"
  }
};
</script>
