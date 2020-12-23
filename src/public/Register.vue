<template>
  <main class="child">
    <form>
      <h1 class="h3 mb-3 fw-normal">Please register</h1>
      <label for="email" class="visually-hidden">Email Address</label>
      <input
        v-model="userDomain.email"
        type="text"
        id="email"
        class="form-control"
        placeholder="Email"
        required
        autofocus
      />
      <label for="firstName" class="sr-only">First Name</label>
      <input
        type="text"
        v-model="userDomain.firstname"
        id="firstName"
        class="form-control"
        placeholder="first name"
        required
      />

      <label for="lasttName" class="sr-only">Last Name</label>
      <input
        type="text"
        v-model="userDomain.lastName"
        id="lastName"
        class="form-control"
        placeholder="last name"
        required
      />

      <label for="inputPassword" class="sr-only">Password</label>
      <input
        v-model="userDomain.password"
        type="password"
        id="inputPassword"
        class="form-control"
        placeholder="Password"
        required
      />
      <label for="inputPassword2" class="visually-hidden">Confirm Password</label>
      <input
        v-model="userDomain.confirmPswd"
        type="password"
        id="inputPassword2"
        class="form-control"
        placeholder="Confirm password"
        required
      />

      <button @click="regBtnClicked()" class="w-100 btn btn-lg btn-primary" type="submit">
        Register
      </button>
      <p class="mt-5 mb-3 text-muted">&copy; 2017-2020</p>
    </form>
  </main>
</template>

<script>
import { reactive } from "vue";
export default {
  name: "Register",
  setup() {
    const userDomain = reactive({
      firstName: "Enter a name",
      lastName: "Enter a surname",
      email: "Enter an email",
      password: "",
      confirmPswd: "",
    });
    function regBtnClicked() {
      alert("Email addr entered: " + userDomain.email);
    }
    return {
      userDomain,
      regBtnClicked,
    };
  },
};
</script>

<style lang="css" scoped>
html,
body {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  padding-top: 40px;
  padding-bottom: 40px;
  background-color: #f5f5f5;
  color: cadetblue;
}

.form-signin {
  width: 100%;
  max-width: 330px;
  padding: 15px;
  margin: auto;
}
.form-signin .checkbox {
  font-weight: 400;
}
.form-signin .form-control {
  position: relative;
  box-sizing: border-box;
  height: auto;
  padding: 10px;
  font-size: 16px;
}
.form-signin .form-control:focus {
  z-index: 2;
}
.form-signin input[type="email"] {
  margin-bottom: -1px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.form-signin input[type="password"] {
  margin-bottom: 10px;
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}

.child {
  width: 400px;
  margin: 0 auto;
}
</style>
