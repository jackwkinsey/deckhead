<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">Deckhead</h1>
      <div class="content">
        <h2>Welcome to Deckhead! <small>Your MTG collection manager</small></h2>
        <super-secret-div v-if="$auth.loggedIn" />
      </div>
    </div>
  </div>
</template>

<script>
import SuperSecretDiv from '~/components/SuperSecretDiv.vue';

export default {
  name: 'Index',
  components: {
    SuperSecretDiv,
  },
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  letter-spacing: 1px;
}

.--small {
  font-size: 40px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
