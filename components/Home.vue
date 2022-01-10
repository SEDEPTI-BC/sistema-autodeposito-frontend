<template>
  <div class="container">
    <div class="title mb-4">
      <h2 class="text-center text-secondary font-weight-light">Deposite seu trabalho acadêmico para que seja publicado através do <strong class="font-weight-bold">Autodeposite</strong></h2>
    </div>
    <div class="headline d-flex flex-column align-items-center flex-wrap my-4 p-4 text-center">
      <h1><img src="~/static/img/brand.png" class="img-fluid ${3|rounded-top,rounded-right,rounded-bottom,rounded-left,rounded-circle,|} mb-4" alt="Autodeposite Brand" title="Autodeposite"></h1>
      <a name="btnHomeLogin" id="btnHomeLogin" class="btn btn-primary btn-lg btn-home-login border-primary text-light font-weight-bold align-self-center" href="/login" role="button">Iniciar depósito</a>
    </div>
    <div class="details mt-4 text-center text-secondary">
      <em class="text-center">Os tipos de trabalhos aceitos são <strong class="font-weight-strongold">TCCs de Graduação e Especialização, Dissertações e Teses</strong></em>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
}
</script>

<style scoped>
.btn-home-login{
  border-radius: 22px;
  width: 246px;
}
</style>