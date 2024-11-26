<template>
  <q-page padding>
    <div class="row justify-center q-gutter-md">
      <div class="col-md-6 col-sm-12">
        <h3 class="text-center">Forgot Password</h3>
        <h5 class="text-center">Enter your registered email below</h5>
        <q-form @submit="onSubmit" class="q-gutter-md">
          <q-input
            v-model="email"
            type="email"
            label="Email"
            :error-message="emailError"
            :counter="255"
          />
          <q-input
            v-model="password"
            type="password"
            label="New Password"
            :error-message="passwordError"
            :counter="255"
          />
          <q-btn
            type="submit"
            label="Submit"
            color="primary"
            expanded
            :disable="!isValid"
          />
        </q-form>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      email: "",
      password: "",
      emailError: "",
      passwordError: "",
    };
  },
  computed: {
    isValid() {
      return this.validateEmail() && this.validatePassword();
    },
  },
  methods: {
    validateEmail() {
      if (this.email === "") {
        this.emailError = "Please enter your email";
        return false;
      } else if (!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(this.email)) {
        this.emailError = "Email tidak valid";
        return false;
      } else {
        this.emailError = "";
        return true;
      }
    },
    validatePassword() {
      if (this.password === "") {
        this.passwordError = "Please enter your password";
        return false;
      } else {
        this.password.length < 8 || !/[A-Z]/.test(this.password);
      }
    },
  },
};
</script>
