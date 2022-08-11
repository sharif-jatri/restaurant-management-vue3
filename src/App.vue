<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link :to="{name: 'signup'}">SignUp</router-link> |
    <router-link :to="{name: 'login'}">Login</router-link>
  </nav>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
