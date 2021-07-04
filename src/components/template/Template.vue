<template>
  <div class="master-border">
    <div class="container">
      <!-- PRIMEIRO ELEMENTO -->
      <div class="elemento1"></div>

      <!-- SEGUNDO ELEMENTO -->
      <div class="container">
        <div class="texto">Opa, amigos!</div>
        <div class="texto">Opa, amigos novamente!</div>
      </div>
      <!-- TERCEIRO ELEMENTO -->
      <div class="container-row">
        <div class="elemento2"></div>
        <div class="elemento2"></div>
        <div class="elemento2"></div>
        <div class="elemento2"></div>
        <div class="elemento2"></div>
        <div class="elemento2"></div>
      </div>

      <!-- QUARTO ELEMENTO -->
      <div class="container">
        <div class="texto">Opa, amigos!</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");

.transition-05 {
  transition: 0.5s;
}

.transition-03 {
  transition: 0.3s;
}

.texto {
  font-family: "Poppins", sans-serif;
  font-size: 1.2rem;
  font-weight: 300;
  color: whitesmoke;
  margin: 10px;
}

.elemento1 {
  margin: 10px;
  width: 150px;
  height: 150px;
  border-radius: 10px;
  background-color: yellow;
}

.elemento2 {
  margin: 10px;
  width: 150px;
  height: 150px;
  border-radius: 10px;
  background-color: blueviolet;
}

.container-row {
  max-width: 510px;
  flex-wrap: wrap;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  flex-wrap: wrap;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.master-border {
  margin-top: 15vh;
  margin-bottom: 50px;
}

.centralize {
  position: absolute;
  top: 50%;
  left: 50%;
  margin-right: -50%;
  transform: translate(-50%, -50%);
}

@media only screen and (max-device-width: 640px) {
  .master-border {
    margin-top: 5vh;
    margin-bottom: 50px;
  }
}
</style>