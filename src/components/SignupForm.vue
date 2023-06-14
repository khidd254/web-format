<template>
  <form>
    <p>signup</p>
    <label>Email:</label>
    <input type="email" required v-model="email">
    <div class="input-container">
      <label for="password">Password:</label>
      <input type="password" id="password" v-model="password" />
    </div>
    <div class="input-container">
      <label for="confirm-password">Confirm Password:</label>
      <input type="password" id="confirm-password" v-model="confirmPassword" />
      <span id="password-error" class="error-message">{{ passwordError }}</span>
    </div><br>
    <div class="terms">
        <input type="checkbox" required v-model="terms">
        <label>Accept terms and conditions</label>
    </div>
    <button class="signup-button" @click.prevent="signUp">Sign Up</button>
   
  </form>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      password: '',
      confirmPassword: '',
      role: 'designer',
      terms: false,
      occupation: '',
      passwordError: ''
    }
  },
  watch: {
    confirmPassword(newVal) {
      if (newVal === this.password) {
        this.passwordError = '';
      }
    }
  },
  methods: {
    signUp() {
      if (!this.validateForm()) {
        return;
      }
      alert('Sign up successful!');
    },
    validateForm() {
      if (!this.email || !this.password || !this.confirmPassword || !this.terms) {
        alert('Please fill in all required fields.');
        return false;
      }
      if (this.password !== this.confirmPassword) {
        this.passwordError = 'Passwords do not match.';
        return false;
      }
      return true;
    }}
  }
</script>
<style>
form{
    max-width: 420px;
    margin: 30px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
}
label{
    color: #aaa;
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
}
input, select {
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color: #555;
}
input[type='checkbox']{
    display: inline-block;
    width: 16px;
    margin: 0 10px 0 0;
    position: relative;
    top: 2px;
}
.signup-button {
      padding: 10px 20px;
      background-color: #0afa87;
      color: white;
      border: none;
      border-radius: 5px;
      font-size: 16px;
      cursor: pointer;
}
.input-container {
      margin-bottom: 10px;
    }
    .error-message {
      color: red;
      font-weight: bold;
    }
</style>