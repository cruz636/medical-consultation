<template>
  <div class="contact-form mt-4">
    <b-card
      @submit.prevent="sendContactMessage()"
      style="border-radius: 8px; width: 50rem"
    >
      <h1 class="display-5" style="font-weight: bold">Necesitas ayuda?</h1>
      <h3 class="mt-3">Contáctenos</h3>
      <b-form-input
        v-model="contact_name"
        class="contact-input"
        placeholder="Nombre"
      />
      <b-form-input
        v-model="contact_email"
        class="contact-input"
        placeholder="Correo"
      />
      <b-form-input
        v-model="contact_phone"
        class="contact-input"
        placeholder="Telefono"
      />
      <b-form-textarea
        v-model="contact_message"
        class="contact-input"
        placeholder="Mensaje"
      />

      <b-button size="lg" class="contact-submit" @click="sendContactMessage">
        <b>Enviar</b>
      </b-button>

      <div v-if="contact_notice != ''" class="alert alert-warning">
        Se produjo un error al enviar el mensaje: {{ this.contact_notice }}
      </div>
      <b-alert
        :show="dismissCountDown"
        class="mt-3"
        dismissible
        variant="green"
        @dismissed="dismissCountDown = 0"
        @dismiss-count-down="countDownChanged"
      >
        Gracias por comunicarte con nosotros, te responderemos lo antes posible.
      </b-alert>
    </b-card>
  </div>
</template>

<script>
export default {
  name: "ContactForm",
  props: {
    title: {
      default: "Contáctenos",
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
      message: "",
      contact_name: "",
      contact_email: "",
      contact_phone: "",
      contact_message: "",
      contact_notice: "",
    };
  },
  methods: {
    countDownChanged(dismissCountDown) {
      this.dismissCountDown = dismissCountDown;
    },
    showSuccess() {
      this.dismissCountDown = this.dismissSecs;
    },
    sendContactMessage() {
      if (this.contact_name.length < 2) {
        this.contact_notice = "Olvidaste tu nombre.";
      } else if (!this.validateEmail(this.contact_email)) {
        this.contact_notice = "El email no es válido.";
      } else if (!this.validatePhone(this.contact_phone)) {
        this.contact_notice = "No es un teléfono válido.";
      } else if (!this.validateMessage(this.contact_message)) {
        this.contact_notice = "El mensaje es muy corto.";
      }
      // TODO: add more valitaions to prevent spam
      else {
        // this.contact_notice = '';
        // let url = `https://us-central1-chiefmining-fb14b.cloudfunctions.net/sendEmail?email_from=${this.contact_email}&name=${this.contact_name}&phone=${this.contact_phone}&message=${this.contact_message}` ;
        // const requestOptions = {
        //     method: "GET",
        //     headers: { "Content-Type": "application/json"}
        // };
        // fetch(url, requestOptions);
        this.showSuccess();
      }
    },
    // form fields validations to prevent spam
    validateEmail(email) {
      const re =
        /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
      return re.test(String(email).toLowerCase());
    },
    validatePhone(number) {
      const re = /^\d{6,12}$/;
      return re.test(String(number));
    },
    validateMessage(message) {
      return message.length > 5;
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