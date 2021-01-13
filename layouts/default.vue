<template>
  <div>
    <!-- <div class="navbar">
      <div class="nav-links">
        <NuxtLink to="/" class="nav-link">Deckhead</NuxtLink>
      </div>
      <div class="login-links">
        <div v-if="$auth.loggedIn">
          {{ $auth.user.email }}
        </div>
        <div v-else>
          <NuxtLink to="/auth/login" class="nav-link">Login</NuxtLink>
          <NuxtLink to="/auth/register" class="nav-link">Register</NuxtLink>
        </div>
      </div>
    </div> -->
    <nav-bar />
    <Nuxt class="app-view" />
  </div>
</template>

<script>
import NavBar from '~/components/NavBar.vue';

export default {
  components: {
    NavBar,
  },
};
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

.navbar {
  position: fixed;
  width: 100%;
  height: 60px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px;
  background-color: #35495e;
  color: #fff;
}

.nav-link {
  text-decoration: none;
}
.nav-link,
.nav-link:visited {
  color: white;
}

.app-view {
  padding-top: 60px;
}
</style>
