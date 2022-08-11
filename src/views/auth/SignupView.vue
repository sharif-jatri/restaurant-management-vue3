<template>
  <h1>Sign Up</h1>
    <form class="form-container" @submit.prevent="formHandler">
      <input type="text" v-model="formData.name" placeholder="Enter Name"/>
      <input type="email" v-model="formData.email" placeholder="Enter Email"/>
      <input type="password" v-model="formData.password" placeholder="Enter Password"/>
      <input type="submit" placeholder="Submit">
  </form>
  <router-link :to="{name: 'login'}">Login</router-link>
</template>

<script>
import {reactive} from "vue";
import axios from "axios";

export default {
  name: 'SignupView',
  setup() {
    const formData = reactive({
      name: null,
      email: null,
      password: null,
    });
    const formHandler = async () => {
      if (formData.name && formData.email && formData.password) {
        const result = await axios.post(process.env.VUE_APP_API+"users", formData);
        if(result.status === 201){
          formData.name = null
          formData.email = null
          formData.password = null
          alert('registration successful')
        }
      } else {
        alert('Please input all values')
      }
    }
    return{
      formData,
      formHandler
    }
  }
}
</script>
