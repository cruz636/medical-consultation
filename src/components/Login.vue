<template>
  <div class="contact-form mt-4">
    <b-card
      @submit.prevent="sendContactMessage()"
      style="border-radius: 8px; width: 50rem"
    >
      <h1 class="display-5" style="font-weight: bold">
        {{ title }}
      </h1>
      <h3 v-if="subtitle" class="mt-3">
        {{ subtitle }}
      </h3>

      <b-form-input
        v-model="contact_email"
        class="contact-input"
        placeholder="Correo"
      />
      <b-form-input
        v-model="password"
        class="contact-input"
        placeholder="contraseña"
      />
      <br />
      <br />

      <b-button size="lg" class="contact-submit mt-4">
        <b>Iniciar Sesion</b>
      </b-button>
    </b-card>
  </div>
</template>

<script>
export default {
  name: "LoginForm",
  props: {
    title: {
      default: "Iniciar Sesión",
      required: false,
    },
    subtitle: {
      required: false,
    },
  },
  data: function () {
    return {
      dismissSecs: 5,
      dismissCountDown: 0,
      email: "",
      password: "",
    };
  },
  methods: {
    countDownChanged(dismissCountDown) {
      this.dismissCountDown = dismissCountDown;
    },
    showSuccess() {
      this.dismissCountDown = this.dismissSecs;
    },

    // form fields validations to prevent spam
    validateEmail(email) {
      const re =
        /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
      return re.test(String(email).toLowerCase());
    },
  },
};
</script>

<style scoped>
.contact-form {
  color: black;
  align-items: center;
  display: flex;
  justify-content: center;
  opacity: 0.9;
}
.contact-input {
  border-bottom: 1px solid black;
  border-top: 0px;
  border-right: 0px;
  border-left: 0px;
  border-radius: 0px;
  margin-top: 15px;
}
.contact-input:hover {
  border-bottom: 2px solid #00cfc89c;
}
.contact-submit {
  background: transparent;
  border: 0px;
  color: black;
  margin-top: 20px;
}
.contact-submit:hover {
  color: #7e056e;
  background: transparent;
  border-bottom: 1px solid #7e056e;
  border-radius: 0px;
}
</style>