<template>
  <div class="row">
    <div class="col-6 register">
      <b-card style="background: transparent; border: 0px">
        <h1 class="display-5" style="font-weight: bold">Registrate</h1>
        <b-form-input
          v-model="password"
          class="contact-input"
          placeholder="Nombre"
          style="background: transparent"
        />
        <b-form-input
          v-model="password"
          class="contact-input"
          placeholder="Apellido"
          style="background: transparent"
        />

        <b-form-input
          v-model="contact_email"
          class="contact-input"
          placeholder="Correo"
          style="background: transparent"
        />
        <br />
        <br />
        <br />
        <br />
        <b-button size="lg" class="contact-submit">
          <b>Regístrate</b>
        </b-button>
      </b-card>
    </div>
    <div class="col-6 login">
      <b-card style="background: transparent; border: 0px">
        <h1 class="display-5" style="font-weight: bold">Iniciar Sesión</h1>
        <b-form-input
          v-model="email"
          class="contact-input-login"
          placeholder="Email"
          style="background: transparent"
        />
        <b-form-input
          v-model="password"
          class="contact-input-login"
          placeholder="Contraseña"
          style="background: transparent"
        />
        <br />
        <br />
        <br />
        <br />
        <br />
        <br />
        <b-button size="lg" class="login-button">
          <b>Iniciar Sesión</b>
        </b-button>
      </b-card>
    </div>
  </div>
</template>
<script>
export default {
  name: "LoginRegisterForm",
};
</script>

<style scoped>
.register {
  color: white;
  background: #00cfc89c;
  min-height: 60vh;
}
.login {
  color: white;
  background: #7e056e;
}
.contact-form {
  color: white;
  align-items: center;
  display: flex;
  justify-content: center;
  opacity: 0.9;
}
.contact-input {
  border-bottom: 1px solid white;
  border-top: 0px;
  border-right: 0px;
  border-left: 0px;
  border-radius: 0px;
  margin-top: 15px;
}
.contact-input:hover {
  border-bottom: 2px solid #00cfc89c;
}
.contact-input-login {
  border-bottom: 1px solid white;
  border-top: 0px;
  border-right: 0px;
  border-left: 0px;
  border-radius: 0px;
  margin-top: 15px;
}
.contact-input-login:hover {
  border-bottom: 2px solid #380231;
}

.login-button {
  border: 0px;
  color: white;
  background: #00cfc8;
  margin-top: 20px;
  width: 50vh;
}
.login-button:hover {
  color: #00cfc8fb;
}
.contact-submit {
  color: white;
  background: #7e056e;
  margin-top: 20px;
  width: 50vh;
}
.contact-submit:hover {
  color: #9e5494;
}
</style>