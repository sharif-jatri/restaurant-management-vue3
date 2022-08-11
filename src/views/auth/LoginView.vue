<template>
  <h1>Login</h1>
  <div class="form-container">
    <input type="email" placeholder="Enter Email"/>
    <input type="password" placeholder="Enter Password"/>
    <button>Register</button>
    <router-link :to="{name: 'signup'}">Sign up</router-link>
  </div>
</template>

<script>
export default {
  name: 'LoginView',

}
</script>
<style>
.form-container input, button{
  display: block;
  margin: 0 850px;
}
</style>
