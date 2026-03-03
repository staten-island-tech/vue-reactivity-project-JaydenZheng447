<template>
  <div>
    <form action="submit" @submit.prevent="login(user)">
      <label for="username">Username</label>
      <input type="text" v-model="user.username" />
      <label for="password">Password</label>
      <input type="password" v-model="user.password" />
      <button type="submit">Login</button>
    </form>
    <h2>Welcome {{ user.username }}</h2>
    <h2>Please Login</h2>
    <h1 v-if="loggedIn">Vue is awesome!{{ loggedIn.username }} and {{ loggedIn.password }}</h1>
    <h1 v-else>Oh no 😢</h1>
  </div>
</template>

<script setup>
//add new ref for loggedIn: Boolean. new function to update that value
import { reactive, ref } from 'vue'
const user = reactive({ username: '', password: '' })
const loggedIn = ref(false)
function login(user) {
  console.log(user)
  loggedIn.value = true
}
</script>

<style lang="css" scoped></style>
