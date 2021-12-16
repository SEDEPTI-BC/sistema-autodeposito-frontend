<template>
  <div class="card p-4">
    <div class="brand text-center">
      <h1><img src="~/static/img/logo.png" class="img-fluid ${3|rounded-top,rounded-right,rounded-bottom,rounded-left,rounded-circle,|}" alt="Autodeposite" title="Autodeposite" width="69" height="46"></h1>
    </div>
    <form method="post" action="">
      <div class="form-group">
        <label for="inputLoginEmail">Email</label>
        <input type="email" class="form-control mx-auto" name="inputLoginEmail" id="inputLoginEmail" placeholder="Informe o seu email">
      </div>
      <div class="form-group">
        <label for="inputLoginPassword">Senha</label>
        <input type="password" class="form-control mx-auto" name="inputLoginPassword" id="inputLoginPassword" aria-describedby="forgetPassword" placeholder="Informe a sua senha">
        <small id="forgetPassword" class="form-text text-muted text-center">Esqueceu sua senha? <a class="text-secondary font-weight-bold" href="#" target="_blank">Clique aqui para recuperar!</a></small>
      </div>
      <div class="form-group text-center">
        <button type="submit" class="btn btn-primary border-primary">Entrar</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {

}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html,
body{
  height: 100%;
  background-image: url('@/static/img/banner.jpeg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
</style>