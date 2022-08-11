<template>
  <h1>Sign Up</h1>
  <div class="form-container">
    <input type="text" placeholder="Enter Name"/>
    <input type="email" placeholder="Enter Email"/>
    <input type="password" placeholder="Enter Password"/>
    <button>Register</button>
    <router-link :to="{name: 'login'}">Login</router-link>
  </div>
</template>

<script>
export default {
  name: 'SignupView',

}
</script>
