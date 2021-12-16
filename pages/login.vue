<template>
  <div class="cadastro bg-light">
    <header>
      <Header />
    </header>
    <main class="centralize col-lg-4 col-md-8 col-xs-12">
      <Login />
    </main>
    <footer class="fixed-bottom p-1">
      <Footer />
    </footer>
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
  overflow-x: hidden;
  overflow-y: scroll;
  scroll-behavior: smooth;
  background-image: url('@/static/img/banner.jpeg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.btn-primary{
  background-color: #93c645;
}

.btn-primary:hover{
  background-color: #9bc957;
}

.border-primary{
  border: #93c645;
}

.centralize{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>