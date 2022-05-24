<template>
  <div class="admin-auth-page">
    <div class="auth-container">
      <form>
         <AppControlInput v-if="!isLogin"  v-elsetype="name">
          <label  >Nome (username)</label>
        </AppControlInput>
        <AppControlInput type="email">
          <label>Indirizzo E-Mail</label>
        </AppControlInput>
        <AppControlInput type="password">
          <label>Password</label></AppControlInput
        >
       <AppControlInput v-if="!isLogin" type="password">
          <label>Conferma Password</label></AppControlInput
        >
        <AppButton   style="margin: 10px"  btn-style="btn-success" type="submit">
        {{ isLogin ? "Login" : "Registrati" }}</AppButton>
<label style="margin:10px"> {{isLogin ? "Non hai ancora un account?" : "Sei già registrato?"}}</label>
        <AppButton
          type="button"
          btn-style="btn-primary"
          style="margin-left: 10px"
          @click="isLogin = !isLogin"
          >Vai a {{ isLogin ? "Registrazione" : "Login" }}</AppButton
        >
      </form>
    </div>
  </div>
</template>

<script>
import AppControlInput from "@/components/UI/AppControlInput";
import AppButton from "@/components/UI/AppButton";

export default {
  name: "AdminAuthPage",
  layout: "admin",
  components: {
    AppControlInput,
    AppButton,
  },
  data() {
    return {
      isLogin: true,
    };
  },
};
</script>

<style scoped>
.admin-auth-page {
  padding: 20px;
}

.auth-container {
  border: 1px solid #ccc;
  border-radius: 5px;
  box-shadow: 0 2px 2px #ccc;
  width: 300px;
  margin: auto;
  padding: 10px;
  box-sizing: border-box;
}
label{
  font-weight:700;
  color:rgb(2, 57, 93)
}
</style>
