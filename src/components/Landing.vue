<template>
  <div class="container-fluid m-0 p-0">
    <div class="d-none d-lg-block">
      <div id="home" class="full-height home p-4">
        <LandingNavBar />
        <br />
        <br />
        <br />
        <br />
        <div class="row mt-4">
          <div class="col-1" />
          <div class="col-6">
            <div class="title">Medical Consultation</div>
            <span>
              <h3>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce
                auctor consequat rutrum. Donec in auctor tortor. Sed fringilla
                ut ex in cursus. Aenean non turpis ut libero sodales faucibus
                vel sed nisi.
              </h3>
            </span>
            <button class="button mt-3">Seguir leyendo</button>
          </div>
        </div>
      </div>
      <br />
      <br />
      <div class="row">
        <div class="col-2" />
        <div class="col-8">
          <hr class="separator" />
        </div>
      </div>
      <div id="servicios" class="medium-height my-4">
        <div class="title mb-3" style="color: rgb(61, 33, 68)">
          Por qué elegirnos?
        </div>
        <div class="row">
          <div class="col-2" />
          <div style="text-align: start" class="col-4">
            <h2 style="font-weight: bold; color: rgb(61, 33, 68)">
              Medicos certificados
            </h2>
            <h4>
              Morbi vehicula, lorem vitae dictum scelerisque, justo arcu congue
              eros, sed aliquam elit mauris nec enim. Praesent accumsan lacus
              vitae pellentesque consequat. Pellentesque sagittis vitae nibh sed
              luctus.
            </h4>
          </div>
          <div class="col-1" />
          <div class="col-3">
            <img
              src="../assets/professional.png"
              class="img-thumbnail"
              style="border: 0px"
            />
          </div>
        </div>
        <br />
        <div class="row my-4">
          <div class="col-2" />
          <div class="col-3">
            <img
              src="../assets/recipe.png"
              class="img-thumbnail"
              style="border: 0px"
            />
          </div>
          <div class="col-1" />
          <div style="text-align: start" class="col-4">
            <h2 style="font-weight: bold; color: rgb(61, 33, 68)">
              Diagnóstico personalizado
            </h2>
            <h4>
              Morbi vehicula, lorem vitae dictum scelerisque, justo arcu congue
              eros, sed aliquam elit mauris nec enim. Praesent accumsan lacus
              vitae pellentesque consequat. Pellentesque sagittis vitae nibh sed
              luctus.
            </h4>
          </div>
        </div>
        <div class="row">
          <div class="col-2" />
          <div style="text-align: start" class="col-4">
            <h2 style="font-weight: bold; color: rgb(61, 33, 68)">
              Contacto directo con el profesional
            </h2>
            <h4>
              Morbi vehicula, lorem vitae dictum scelerisque, justo arcu congue
              eros, sed aliquam elit mauris nec enim. Praesent accumsan lacus
              vitae pellentesque consequat. Pellentesque sagittis vitae nibh sed
              luctus.
            </h4>
          </div>
          <div class="col-1" />
          <div class="col-3">
            <img
              src="../assets/messages.png"
              class="img-thumbnail"
              style="border: 0px"
            />
          </div>
        </div>
        <br />
        <div class="row mt-4">
          <div class="col-2" />
          <div class="col-3">
            <img
              src="../assets/hospital.png"
              class="img-thumbnail"
              style="border: 0px"
            />
          </div>
          <div class="col-1" />
          <div style="text-align: start" class="col-4">
            <h2 style="font-weight: bold; color: rgb(61, 33, 68)">
              El profesional directamente en tu hogar
            </h2>
            <h4>
              Morbi vehicula, lorem vitae dictum scelerisque, justo arcu congue
              eros, sed aliquam elit mauris nec enim. Praesent accumsan lacus
              vitae pellentesque consequat. Pellentesque sagittis vitae nibh sed
              luctus.
            </h4>
          </div>
        </div>
      </div>
      <br />
      <br />
      <br />
      <div class="row">
        <div class="col-2" />
        <div class="col-8">
          <hr class="separator" />
        </div>
      </div>
      <br />
      <br />
      <div id="estadisticas" class="medium-height">
        <div><h1>Algunas estadísticas nuestras</h1></div>
        <br />
        <br />
        <div class="row">
          <div class="col-2" />
          <div class="col-2">
            <h1>5125</h1>
            <img
              src="../assets/heart.png"
              class="img-thumbnail"
              style="border: 0px; height: 50%"
            />
            <h3>Usuarios</h3>
          </div>
          <div class="col-2">
            <h1>4115</h1>
            <img
              src="../assets/prognosis.png"
              class="img-thumbnail"
              style="border: 0px; height: 50%"
            />
            <h3>Diagnósticos</h3>
          </div>
          <div class="col-2">
            <h1>243</h1>
            <img
              src="../assets/sthetoscope.png"
              class="img-thumbnail"
              style="border: 0px; height: 50%"
            />
            <h3>Profesionales</h3>
          </div>
          <div class="col-2">
            <h1>4000</h1>
            <img
              src="../assets/survey.png"
              class="img-thumbnail"
              style="border: 0px; height: 50%"
            />
            <h3>Recetas</h3>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-2" />
        <div class="col-8">
          <hr class="separator" />
        </div>
      </div>
      <div id="contact" class="medium-height mb-4">
        <ContactForm />
      </div>
      <br />
      <br />
      <Footer />
    </div>
  </div>
</template>

<script>
import LandingNavBar from "./LandingNavBar";
import ContactForm from "./ContactForm.vue";
import Footer from "./Footer.vue";

export default {
  name: "Landing",
  components: {
    LandingNavBar,
    ContactForm,
    Footer,
  },
};
</script>

<style scoped>
.full-height {
  min-height: 100vh;
}
.medium-height {
  min-height: 60vh;
}
.small-height {
  max-height: 40vh;
}
.home-mv {
  background: url("../assets/home.jpg") no-repeat center center;
  background-size: cover;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
}
.home {
  background: url("../assets/home.jpg") no-repeat center center;
  background-size: cover;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
}

.title {
  font-size: 8vh;
  font-weight: bold;
}

.separator {
  color: #00cfc9;
  height: 3px;
}

/* Move to style.css (below)*/
.register-button {
  width: 50vh;
}
.register-button:hover {
  background: #dedfe6;
}
/* Move to style.css */
.button {
  background: #00cfc9;
  border: 0px solid;
  border-radius: 19px;
  color: #fbfbfb;
  font-size: 3vh;
  height: 6vh;
  width: 30vh;
}
.button:hover {
  color: #fbfbfb;
  background: #00cfc8bd;
  border-bottom: 1px solid;
}
/* Move to style.css */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 1.5s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>