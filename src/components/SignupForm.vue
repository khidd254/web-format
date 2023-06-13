<template>
  <form>
    <label>Email:</label>
    <input type="email" required v-model="email">
    <label>Password:</label>
    <input type="password" required v-model="password">
    <label>Role:</label><br>
    <select v-model="role">
        <option value="developer">Web developer</option>
        <option value="designer">Web Designer</option>
    </select>
    <label>Occupation</label>
    <select v-model="occupation">
        <option value="student">Student</option>
        <option value="self-employment">Self-employed</option>
        <option value="employed">Employed</option>
        <option value="not say">Rather not say</option>
    </select>
    <div class="terms">
        <input type="checkbox" required v-model="terms">
        <label>Accept terms and conditions</label>
    </div>
    <button class="signup-button">Sign Up</button>
   
  </form>
</template>

<script>
export default {
    data(){
        return {
            email: '',
            password: '',
            role: 'designer',
            terms: false,
            occupation: ''
        }
    }
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
}.signup-button {
      padding: 10px 20px;
      background-color: #0afa87;
      color: white;
      border: none;
      border-radius: 5px;
      font-size: 16px;
      cursor: pointer;
}
</style>