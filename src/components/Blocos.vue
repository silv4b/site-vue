<template>
  <div class="centering container flex flex-column">
    <div class="flex-column">
      <div class="big-card">
        <div class="banner"></div>
        <div class="profile flex flex-end"></div>
      </div>
      <div class="social-cards flex flex-row space-between">
        <div class="social flex center">
          <a
            href="https://www.linkedin.com/in/silv4b/"
            target="_blank"
            class="home__social-icon"
          >
            <i class="bx bxl-linkedin-square"></i>
          </a>
        </div>
        <div class="social flex center">
          <a
            href="https://www.instagram.com/uisilvab/"
            target="_blank"
            class="home__social-icon"
          >
            <i class="bx bxl-instagram"></i>
          </a>
        </div>
        <div class="social flex center">
          <a
            href="https://www.figma.com/@silv4b"
            target="_blank"
            class="home__social-icon"
          >
            <i class="bx bxl-figma"></i>
          </a>
        </div>
        <div class="social flex center">
          <a
            href="https://github.com/silv4b"
            target="_blank"
            class="home__social-icon"
          >
            <i class="bx bxl-github"></i>
          </a>
        </div>
        <div class="social flex center">
          <a
            href="https://gitlab.com/silv4b"
            target="_blank"
            class="home__social-icon"
            alt="OPA"
          >
            <i class="bx bxl-gitlab"></i>
          </a>
        </div>
        <div class="social flex center">
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
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "src/style.scss";

.profile {
  width: 100px;
  height: 100px;
  border: 6px;
  border-radius: 100%;
  border-style: solid;
  border-color: $primary-color;
  background-image: url("https://avatars.githubusercontent.com/u/17997794?v=4");
  background-size: 100px 100px;
  margin: -50px 0 0 20px;
}

.banner {
  width: 100%;
  height: 100px;
  background-color: whitesmoke;
  border-radius: 10px 10px 0 0;
  box-shadow: 0px 0px 21px -2px rgba(0, 0, 0, 0.85);
}

.big-card {
  font-size: 2rem;
  width: 500px;
  height: 530px; //height: auto !important;
  background: $primary-color;
  border-radius: 5px;
  box-shadow: 0px 0px 21px -2px rgba(12, 12, 12, 0.85);
  margin-bottom: 30px;
  transition: transform 0.5s;
}

.big-card:hover {
  transform: scale(1.02);
}

.centering {
  height: 90vh;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.social {
  display: flex;
  width: 60px;
  height: 60px;
  border-radius: 5px;
  background-color: $primary-color;
  transition: 0.2s ease-in;
}

.social:hover {
  transform: scale(1.25);
  background-color: whitesmoke;
  .home__social-icon {
    color: $primary-color;
  }
}

.home__social-icon {
  display: flex;
  justify-content: center;
  align-items: center;
  width: max-content;
  font-size: 2rem;
  color: whitesmoke;
  text-decoration: none;
  transition: 0.2s ease-out;
}
</style>