<template>
  <b-navbar toggleable="lg">
    <!-- web navBar-->
    <div class="d-none d-lg-flex mx-auto d-sm-flex d-block flex-sm-nowrap">
      <b-navbar-brand class="d-none d-lg-block">
        <b-button id="medicalConsultation" to="/">
          Medical Consultation
        </b-button>
      </b-navbar-brand>
      <b-navbar-nav class="collapse navbar-collapse text-center">
        <b-nav-item href="#">
          <b-button class="button" :to="home"> Home </b-button>
        </b-nav-item>
        <b-nav-item :href="nosotros">
          <b-button class="button">Nosotros</b-button>
        </b-nav-item>
        <b-nav-item href="#">
          <b-button class="button" :to="blog"> Blog </b-button>
        </b-nav-item>
        <b-nav-item :href="contacto">
          <b-button class="button">Contacto</b-button>
        </b-nav-item>

        <b-nav-item href="#">
          <b-button class="solid-button">Iniciar Sesion</b-button>
        </b-nav-item>
        <b-nav-item href="#">
          <b-button class="solid-button-register">Registrarse</b-button>
        </b-nav-item>
        <b-nav-item-dropdown text="Lang" right>
          <b-dropdown-item href="#">EN</b-dropdown-item>
          <b-dropdown-item href="#">ES</b-dropdown-item>
          <b-dropdown-item href="#">PR</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
    </div>
    <!--Mobile navBar-->
    <!-- <b-container class="d-block d-lg-none">
      <b-row class="text-center">
        <b-col cols="3">
          <div class="btn-group" role="group">
            <button
              type="button"
              class="btn button dropdown-toggle"
              data-toggle="dropdown"
              aria-haspopup="true"
              aria-expanded="false"
            >
              <b-icon icon="list" style="color: #dedfe6" />
            </button>
            <div class="dropdown-menu" aria-labelledby="btnGroupDrop1">
              <a class="dropdown-item" v-if="home">
                <b-button class="dropdown-mobile-button" to="/">
                  Home
                </b-button>
              </a>
              <a class="dropdown-item" v-if="nosotros" :href="nosotros">
                <b-button class="dropdown-mobile-button"> Nosotros </b-button>
              </a>
              <a class="dropdown-item">
                <b-button
                  class="dropdown-mobile-button"
                  v-if="management"
                  to="management"
                >
                  Management
                </b-button>
              </a>
              <a class="dropdown-item" v-if="monitoreo" :href="monitoreo">
                <b-button class="dropdown-mobile-button"> Monitoreo </b-button>
              </a>
              <a class="dropdown-item" :href="contacto">
                <b-button class="dropdown-mobile-button"> Contacto </b-button>
              </a>
            </div>
          </div>
        </b-col>
        <b-col cols="8">
          <b-button style="background: transparent; border: 0px" to="/">
            <h4 style="font-weight: bold">CHIEF MINING</h4>
          </b-button>
        </b-col>
      </b-row>
    </b-container> -->
  </b-navbar>
</template>

<script>
export default {
  name: "LandingNavBar",
};
</script>

<style scoped>
h1 {
  color: #dedfe6;
}
.solid-button {
  background: #ffffff;
  color: #7e056e;
  font-weight: bold;
  border-radius: 15px;
  border: 1px solid;
}
.solid-button:hover {
  color: #7e056e;
  background: whitesmoke;
}
.solid-button-register {
  background: #7e056e;
  color: white;
  font-weight: bold;
  border-radius: 15px;
  border: 1px solid;
}
.solid-button-register:hover {
  background: #ca64bd;
}
.button {
  background: transparent;
  border: 0px solid;
  color: black;
  font-size: 3vh;
}
.button:hover {
  color: #7e056e;
  background: transparent;
  border-radius: 0;
  border-bottom: 1px solid;
}
#medicalConsultation {
  color: rgb(61, 33, 68);
  font-size: 5vh;
  font-weight: bold;
  background: transparent;
  border: 0px;
}
.dropdown-mobile-button {
  color: #ffffff;
  background: transparent;
  border: 0px solid;
  font-size: 10px;
}
</style>