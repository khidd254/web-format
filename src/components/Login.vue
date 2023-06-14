<template>
  <div class="login-container">
    <h2>Login</h2>
    <div class="input-container">
      <label for="email">Email:</label>
      <input type="email" id="email" required v-model="email">
    </div>
    <div class="input-container">
      <label for="password">Password:</label>
      <input type="password" id="password" required v-model="password">
    </div>
    <button class="login-button" @click="login">Login</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showLogin: true,
      email: '',
      password: ''
    }
  },
  methods: {
    login() {
      // Perform login actions or submit the login form
      if (this.email && this.password) {
        // Authentication logic goes here
        alert('Login successful!');
      } else {
        alert('Please enter email and password.');
      }
    }
  }
}
</script>

<style scoped>
.login-container {
  max-width: 420px;
  margin: 30px auto;
  background: white;
  text-align: left;
  padding: 40px;
  border-radius: 10px;
}
h2 {
  color: #aaa;
  font-size: 1.2em;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
  margin-bottom: 20px;
}
input {
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid #ddd;
  color: #555;
  margin-bottom: 10px;
}
.login-button {
  padding: 10px 20px;
  background-color: #0afa87;
  color: white;
  border: none;
  border-radius: 5px;
  font-size: 16px;
  cursor: pointer;
}
</style>