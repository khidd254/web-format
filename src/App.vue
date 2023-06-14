<template>
  <div id="app">
    <div class="form-container">
      <div class="form-wrapper">
        <SignupForm v-if="showSignup" />
      </div>
      <div class="form-wrapper">
        <Login v-if="showLogin" />
      </div>
    </div>
  </div>
</template>
<script>
import SignupForm from './components/SignupForm.vue';
import Login from './components/Login.vue';
export default {
  name: 'App',
  components: {
    SignupForm,
    Login
  },
  data() {
    return {
      showSignup: true,
      showLogin: true
    };
  }
}
</script>

<style>
#app {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
}
.form-container {
  display: flex;
}
.form-wrapper {
  flex: 1;
  margin-right: 10px;
}
.form-wrapper:last-child {
  margin-right: 0;
}
body{
  margin: 0;
  background-color: #eee;
}
</style>
