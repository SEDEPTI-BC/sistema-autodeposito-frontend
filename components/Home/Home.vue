<template>
  <div class="container">
    <div class="title mb-4">
      <h3 class="text-center font-weight-light">Deposite seu trabalho acadêmico para que seja publicado através do <b class="font-weight-bold">Autodeposite</b></h3>
    </div>
    <div class="headline d-flex flex-column align-items-center flex-wrap my-4 p-4 text-center">
      <img src="~/static/img/brand.png" class="img-fluid ${3|rounded-top,rounded-right,rounded-bottom,rounded-left,rounded-circle,|} mb-4" alt="Autodeposite Brand">
      <a name="btnHomeLogin" id="btnHomeLogin" class="btn btn-primary btn-lg btn-home-login border-primary text-light font-weight-bold align-self-center" href="/login" role="button">Iniciar depósito</a>
    </div>
    <div class="details mt-4">
      <h5 class="text-center font-italic">Os tipos de trabalhos aceitos são <b class="font-weight-bold">TCCs de Graduação e Especialização, Dissertações e Teses</b></h5>
    </div>
  </div>
</template>

<script>
export default {}

</script>

<style scoped>
.btn-home-login{
  border-radius: 22px;
  width: 246px;
}
</style>