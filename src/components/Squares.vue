<template>
  <div class="master-border">
    <div class="container">
      <!-- PRIMEIRO ELEMENTO -->
      <div class="container">
        <div class="profile"></div>
      </div>

      <!-- SEGUNDO ELEMENTO -->
      <div class="container">
        <div class="text-name">Bruno Silva | @silv4b</div>
        <div class="text-job">User Interface Designer</div>
      </div>

      <!-- TERCEIRO ELEMENTO -->
      <div class="container-row">
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
      </div>
    </div>

    <!-- QUARTO ELEMENTO -->
    <div class="container">
      <div class="text-bottom">Feito com amor 👨‍💻.</div>
      <div class="logo-img">
        <img
          src="https://raw.githubusercontent.com/silv4b/site-vue/main/src/assets/logo.svg?token=AEJJ7YTFN45YRGXULCXQO5TA5NOSQ"
          alt=""
        />
      </div>
    </div>

    <!-- QUINTO ELEMENTO -->
    <div class="container"></div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "src/style-new.scss";

.profile {
  margin-bottom: 0 !important;
  width: 150px;
  height: 150px;
  background-image: url(https://avatars.githubusercontent.com/u/17997794?v=4);
  background-size: 150px 150px;
  border: 6px;
  border-radius: 100%;
  border-style: solid;
  border-color: $primary-color;
  transition: 0.2s ease-in-out;
}

.profile:hover {
  transform: scale(1.1);
}

.text-name {
  margin-top: 30px;
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

.center {
  justify-content: center;
  align-items: center;
}

.text-bottom {
  margin: 30px;
  font-size: 0.9rem;
  font-weight: 100;
  color: $white-color;
  letter-spacing: 1px;
}

.logo-img img {
  width: 50px;
  height: 50px;
}
</style>
