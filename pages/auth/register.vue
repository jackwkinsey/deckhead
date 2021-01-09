<template>
  <div class="container">
    <h1 class="title --small">Register</h1>
    <div>
      <form @submit.prevent="registerUser">
        <label>
          Name
          <input v-model="name" type="text" placeholder="Jane Doe" />
        </label>
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
        <button type="submit">Register</button>
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
      name: '',
      password: '',
    };
  },
  methods: {
    registerUser() {
      console.log(
        `register user with ${this.name}, ${this.email} & ${this.password}`
      );
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
