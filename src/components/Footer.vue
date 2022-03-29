<template>
  <footer class="page-footer small-height font-small pt-4">
    <!-- Mobile Footer-->
    <div class="d-block d-lg-none container-fluid text-center">
      <h1 style="font-weight: bold">Medical Consultation</h1>
      <ul class="list-unstyled mt-4">
        <li>chiefwebmine@gmail.com</li>
        <li>Av. Luis Maria Campos 1053, BOI, CABA, Argentina.</li>
        <li>Whatsapp: +54 9 11 3132-5690</li>
      </ul>
      <div class="footer-copyright text-center py-3">
        © 2022 Copyright: Medical Consultation
      </div>
    </div>

    <!-- Web Footer -->
    <div class="d-none d-lg-block container-fluid text-center">
      <!-- Grid row -->
      <br />
      <div class="row">
        <!-- Grid column -->
        <div class="col-3" />
        <div class="col-3 mt-3">
          <!-- Content -->
          <h2 style="font-weight: bold">Medical Consultation</h2>
          <div class="footer-copyright text-center py-3">
            © 2022 Copyright: Medical Consultation
          </div>
        </div>

        <div class="col-6 mb-md-0 mb-3" style="text-align: start">
          <!-- Links -->
          <br />
          <h5 style="font-weight: bold" class="ml-5">Contacto</h5>
          <ul class="list-unstyled">
            <li>info@medicalconsultation.com</li>
            <li>Ciudad Autónoma de Buenos Aires, Argentina.</li>
            <li>Whatsapp: +54 9 11 3132-5690</li>
          </ul>
        </div>
        <!-- Grid column -->
      </div>
      <!-- Grid row -->
    </div>
    <!-- Footer Links -->
  </footer>
  <!-- Footer -->
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
.text-footer {
  color: #dedfe6;
}
.small-height {
  min-height: 40vh;
  /* background: #282525; */
  background: #00cfc9;
}
.solid-button {
  background: transparent;
  border: 1px solid;
}
.solid-button:hover {
  background: #dedfe6;
  color: #111211;
}
.button {
  background: transparent;
  border: 0px solid;
  color: #fbfbfb;
  padding-bottom: 2px;
}
.button:hover {
  color: #fbfbfb;
  border-radius: 0;
  border-bottom: 1px solid;
}
li {
  margin-top: 5px;
}
</style>