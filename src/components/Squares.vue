<template>
  <div class="centering flex">
    <div class="flex-column">
      <div class="flex space-around">
        <div class="profile flex center"></div>
      </div>
      <div class="text-name">Bruno Silva | @silv4b</div>
      <div class="text-job">User Interface Designer</div>
      <div class="social-cards flex flex-row space-around wrap">
        <div class="social-cards flex flex-row space-around wrap">
          <div class="social center">
            <a
              href="https://www.linkedin.com/in/silv4b/"
              target="_blank"
              class="home__social-icon"
            >
              <i class="bx bxl-linkedin-square"></i>
            </a>
          </div>
          <div class="social center">
            <a
              href="https://www.instagram.com/uisilvab/"
              target="_blank"
              class="home__social-icon"
            >
              <i class="bx bxl-instagram"></i>
            </a>
          </div>
          <div class="social center">
            <a
              href="https://www.figma.com/@silv4b"
              target="_blank"
              class="home__social-icon"
            >
              <i class="bx bxl-figma"></i>
            </a>
          </div>
          <div class="social center">
            <a
              href="https://github.com/silv4b"
              target="_blank"
              class="home__social-icon"
            >
              <i class="bx bxl-github"></i>
            </a>
          </div>
          <div class="social center">
            <a
              href="https://gitlab.com/silv4b"
              target="_blank"
              class="home__social-icon"
              alt="OPA"
            >
              <i class="bx bxl-gitlab"></i>
            </a>
          </div>
          <div class="social center">
            <a
              href="mailto:brunoxbkd@gmail.com"
              target="_blank"
              class="home__social-icon"
            >
              <i class="bx bx-mail-send"></i>
            </a>
          </div>
          <div class="social center">
            <a
              href="https://twitter.com/silv4b"
              target="_blank"
              class="home__social-icon"
            >
              <i class="bx bxl-twitter"></i>
            </a>
          </div>
          <div class="social center">
            <a
              href="https://dribbble.com/silvab"
              target="_blank"
              class="home__social-icon"
            >
              <i class="bx bxl-dribbble"></i>
            </a>
          </div>
          <div class="social center">
            <a
              href="https://open.spotify.com/playlist/7FCrKytZs7U3Mm4WXWabVm"
              target="_blank"
              class="home__social-icon"
            >
              <i class="bx bxl-spotify"></i>
            </a>
          </div>
        </div>
        <div class="flex column center">
          <div class="text-bottom">Feito com amor 💖.</div>
          <div class="logo-img"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "src/style.scss";

.text-name {
  margin-top: 30px;
  margin-bottom: 10px;
  font-size: 1.5rem;
  font-weight: 400;
  color: $white-color;
}

.text-job {
  margin: 10px;
  margin-bottom: 20px;
  font-size: 1rem;
  color: $secondary-color;
  font-weight: 300;
}

.text-bottom {
  margin: 30px;
  font-size: 0.9rem;
  font-weight: 100;
  color: $white-color;
  letter-spacing: 1px;
}

.logo-img {
  width: 50px;
  height: 50px;
  background-size: 50px 50px;
  background-image: url(https://raw.githubusercontent.com/silv4b/site-vue/main/src/assets/logo.png?token=AEJJ7YQZPCOCZRELOMUROPTA4YYYU);
  margin-bottom: 40px;
}

.profile {
  margin: 70px;
  margin-bottom: 30px;
  width: 150px;
  height: 150px;
  background-image: url(https://avatars.githubusercontent.com/u/17997794?v=4);
  background-size: 150px 150px;
  border: 6px;
  border-radius: 100%;
  border-style: solid;
  transition: 0.5s;
  border-color: $primary-color;
}

.centering {
  height: 90vh;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.social {
  display: flex;
  width: 100px;
  height: 100px;
  border-radius: 8px;
  background-color: $primary-color;
  transition: 0.17s ease-in;
  margin: 20px;
}

.social:hover {
  transform: scale(1.2);
  border-radius: 10px !important;
  background-color: $white-color;
  .home__social-icon {
    color: $primary-color;
  }
}

.social-cards {
  max-width: 500px;
  display: flex;
}

.home__social-icon {
  display: flex;
  justify-content: center;
  align-items: center;
  width: max-content;
  font-size: 3rem;
  color: $white-color;
  text-decoration: none;
  transition: 0.2s ease-out;
}
</style>
