<template>
  <div class="signup card p-4">
    <div class="brand text-center">
      <h1><img src="~/static/img/logo.png" class="img-fluid ${3|rounded-top,rounded-right,rounded-bottom,rounded-left,rounded-circle,|}" alt="Autodeposite" title="Autodeposite" width="69" height="46"></h1>
    </div>
    <form method="post" action="">
      <small class="form-text text-muted text-center">Campos obrigatórios são marcados com *</small>
      <div class="form-group">
        <label for="inputSignupName">Informe seu nome completo *</label>
        <input type="text" class="form-control mx-auto" name="inputSignupName" id="inputSignupName" v-model="inputSignupName" required>
      </div>
      <div class="form-group">
        <label for="inputSignupEmail">Informe seu email *</label>
        <input type="email" class="form-control mx-auto" name="inputSignupEmail" id="inputSignupEmail" v-model="inputSignupEmail" required>
      </div>
      <div class="form-group">
        <label for="inputSignupPassword">Crie sua senha *</label>
        <input type="password" class="form-control mx-auto" name="inputSignupPassword" id="inputSignupPassword" v-model="inputSignupPassword" required>
      </div>
      <div class="form-group">
        <label for="inputSignupPasswordConfirm">Confirme sua senha *</label>
        <input type="password" class="form-control mx-auto" name="inputSignupPasswordConfirm" id="inputSignupPasswordConfirm" v-model="inputSignupPasswordConfirm" required>
      </div>
      <div class="form-group text-center">
        <button type="submit" class="btn btn-primary border-primary">Entrar</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Signup',
  data() {
    return {
      inputSignupName: '',
      inputSignupEmail: '',
      inputSignupPassword: '',
      inputSignupPasswordConfirm: '',
    }
  },
  methods: {
  },
}
</script>

<style>

</style>