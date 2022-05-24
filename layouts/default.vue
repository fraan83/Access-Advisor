<template>
  <div class="bg-landing">
    <Navbar />
    <div class="main_container ">
    <nuxt />
    </div>


  </div>
</template>
<script>
import Navbar from "@/components/Navbar.vue";
import AppButton from "@/components/UI/AppButton.vue";
import Footer from "@/components/sections/Footer.vue";
export default {
  components: {
    Navbar,
    Footer,
    AppButton
  },
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&display=swap");

html {
  font-family: "Lato", sans-serif !important;
}
.main_container {
    display: flex;
    max-width: 1366px;
    justify-content: center;
    align-items: stretch;
    align-content: stretch;
    flex-direction: column;
    flex-wrap: nowrap;
    margin: 0 auto;
}
.bg-landing {
  width: 100%;
  height: auto;
  top: 0;
  left: 0;
  background: url(/images/bg-lading-up.svg) no-repeat center top;
  position: absolute;
  z-index: -1;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  margin: 0 auto;
}
</style>
