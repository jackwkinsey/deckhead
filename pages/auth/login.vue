<template>
  <div class="container">
    <h1 class="title --small">Login</h1>
    <div>
      <form @submit.prevent="loginUser">
        <label>
          Email
          <input v-model="email" type="text" placeholder="user@email.com" />
        </label>
        <label>
          Password
          <input
            v-model="password"
            type="password"
            placeholder="enter password"
          />
        </label>
        <button type="submit">Login</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data() {
    return {
      email: '',
      password: '',
    };
  },
  methods: {
    loginUser() {
      console.log(`login user with ${this.email} & ${this.password}`);
    },
  },
};
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
  align-items: center;
}
input {
  width: 300px;
  display: block;
  padding: 3px;
  border: 1px solid black;
}
label {
  margin: 10px;
}
button {
  padding: 10px;
}

.container {
  flex-direction: column;
}
</style>
