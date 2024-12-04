<template>
  <q-page class="otp-page">
    <div class="otp-container">
      <!-- Header -->
      <h2 class="text-h5 text-center row justify-center q-mt-xl">
        <b> Verification</b>
      </h2>
      <p class="text-center">
        Enter the verification code sent via SMS to your phone number
      </p>
      <div class="otp-phone-number text-center row justify-center q-mt-xl">
        +62 xxxx xxxx
      </div>

      <!-- OTP Input Fields -->
      <div class="otp-inputs row justify-center q-mt-xl">
        <q-input
          v-for="(digit, index) in otpDigits"
          :key="index"
          v-model="otp[index]"
          type="password"
          maxlength="1"
          dense
          outlined
          class="otp-digit"
          ref="otpField"
          @keyup="focusNext(index, $event)"
        />
      </div>

      <!-- Timer -->
      <div class="timer text-center q-mt-md">
        {{ formattedTime }}
      </div>

      <!-- Confirmation Button -->
      <q-btn
        label="Confirmation"
        color="primary"
        class="q-mt-lg"
        style="width: 100%"
        @click="verifyOtp"
      />
    </div>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      otp: Array(6).fill(""), // Holds the 6-digit OTP
      otpDigits: Array(6).fill(null), // Dummy array for rendering inputs
      countdown: 150, // Timer in seconds (2:30 = 150 seconds)
    };
  },
  computed: {
    formattedTime() {
      const minutes = String(Math.floor(this.countdown / 60)).padStart(2, "0");
      const seconds = String(this.countdown % 60).padStart(2, "0");
      return `${minutes}:${seconds}`;
    },
  },
  methods: {
    focusNext(index, event) {
      // Move to the next input if the current one has a value
      if (event.target.value.length === 1 && index < this.otp.length - 1) {
        this.$refs.otpField[index + 1].$el.querySelector("input").focus();
      }

      // Handle backspace to move focus to the previous input
      if (event.key === "Backspace" && event.target.value === "" && index > 0) {
        this.$refs.otpField[index - 1].$el.querySelector("input").focus();
      }
    },
    verifyOtp() {
      const otpCode = this.otp.join("");
      if (otpCode.length === 6) {
        // Trigger OTP verification logic here
        console.log("OTP Submitted:", otpCode);
      } else {
        this.$q.notify({
          message: "Please enter all 6 digits",
          type: "negative",
        });
      }
    },
  },
  mounted() {
    // Start the countdown timer
    this.startTimer();
  },
  methods: {
    startTimer() {
      const interval = setInterval(() => {
        if (this.countdown > 0) {
          this.countdown -= 1;
        } else {
          clearInterval(interval); // Stop the timer at 0
          this.$q.notify({
            message: "Time expired. Please request a new OTP.",
            type: "warning",
          });
        }
      }, 1000);
    },
  },
};
</script>

<style scoped>
.otp-container {
  max-width: 400px;
  margin: auto;
  text-align: center;
}

.otp-inputs {
  gap: 10px;
}

.otp-digit {
  width: 50px;
  text-align: center;
}
.timer {
  font-size: 1.2rem;
  color: #555;
  font-weight: bold;
}
</style>
