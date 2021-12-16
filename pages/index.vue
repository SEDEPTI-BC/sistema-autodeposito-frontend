<template>
  <HomePage />
</template>

<script>
export default {}
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

.btn-primary{
  background-color: #93c645;
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