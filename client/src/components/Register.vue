<template>
  <div>
    <h1>Register</h1>
    <input type="email" name="email" placeholder="email" v-model="email">
    <br>
    <input type="password" name="password" placeholder="password" v-model="password">
    <br>
    <button @click="register">Register</button>
  </div>
</template>

<script>
import AuthenticationService from '@/services/AuthenticationService'
export default {
  data() {
    return {
      email: '',
      password: ''
    }
  },
  watch: {
    email(value) {
      console.log('Mudou', value)
    }
  },
  methods: { register() { console.log('Clicado Registrar', this.email, this.password) } }
}
</script>

<style scoped></style>
