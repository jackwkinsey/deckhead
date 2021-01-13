<template>
  <div class="header">
    <nuxt-link to="/" exact>Home</nuxt-link>
    <a v-if="$auth.loggedIn" @click="$auth.logout()">Log Out</a>
    <a v-else @click="$auth.loginWith('auth0')">Log In</a>
  </div>
</template>

<script>
export default {};
</script>

<style>
.header {
  display: flex;
  margin-bottom: 20px;
}
</style>
