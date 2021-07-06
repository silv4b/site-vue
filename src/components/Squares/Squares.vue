<template>
  <div class="master-border">
    <div class="container">
      <!--  PERFIL -->
      <div class="container">
        <div class="profile"></div>
      </div>

      <!-- TEXTOS -->
      <div class="container">
        <div class="text-name">{{ texts[0] }}</div>
        <div class="text-job">{{ texts[1] }}</div>
      </div>

      <!-- REDES SOCIAIS -->
      <div class="container-row">
        <div v-for="sl in socialList" v-bind:key="sl.id" :class="classCard">
          <a :href="sl.href" target="_blank" :class="classSocialIcons">
            <i :class="sl.iclass"></i>
          </a>
        </div>
      </div>

      <!-- PLAYLIST 
      <div class="container">
        <div type="button" @click="spotifyLink()" class="spotify-button">
          <div class="container-row">
            <a class="social_icon_style_2"><i class="bx bxl-spotify"></i> </a>
          </div>
        </div>
      </div> -->

      <!-- MODAL -->
      <div class="container">
        <div
          type="button"
          @click="$refs.modalName.openModal()"
          class="spotify-button"
        >
          <div class="container-row">
            <a class="social_icon_style_2"><i class="bx bxs-playlist"></i> </a>
            <div class="change_later"></div>
          </div>
        </div>
        <modal ref="modalName">
          <template v-slot:header>
            <h1>Playlists</h1>
          </template>
          <template v-slot:body>
            <p>Lorem ipsum dolor sit amet.</p>
          </template>
        </modal>
      </div>

      <!-- TEXTO E LOGO -->
      <div class="container">
        <div class="text-bottom">{{ texts[2] }}</div>
        <div class="logo-img">
          <img
            src="https://raw.githubusercontent.com/silv4b/site-vue/main/src/assets/logo.svg?token=AEJJ7YTFN45YRGXULCXQO5TA5NOSQ"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Modal from "../Modal/Modal.vue";

export default {
  components: {
    Modal,
  },
  methods: {
    spotifyLink: function () {
      window.open(
        "https://open.spotify.com/playlist/7FCrKytZs7U3Mm4WXWabVm?si=ad49b6d20e134832&nd=1",
        "_blank"
      );
    },
  },
  data() {
    return {
      classCard: "social center",
      classSocialIcons: "social_icon_style",
      texts: [
        "Bruno Silva | @silv4b",
        "User Interface Designer",
        "Feito com amor 👨‍💻",
      ],
      socialList: [
        {
          id: 1,
          social: "LinkedIn",
          href: "https://www.linkedin.com/in/silv4b/",
          iclass: "bx bxl-linkedin-square",
        },
        {
          id: 2,
          social: "Instagram",
          href: "https://www.instagram.com/uisilvab/",
          iclass: "bx bxl-instagram",
        },
        {
          id: 3,
          social: "Figma",
          href: "https://www.figma.com/@silv4b",
          iclass: "bx bxl-figma",
        },
        {
          id: 4,
          social: "Github",
          href: "https://github.com/silv4b",
          iclass: "bx bxl-github",
        },
        {
          id: 5,
          social: "Gitlab",
          href: "https://gitlab.com/silv4b",
          iclass: "bx bxl-gitlab",
        },
        {
          id: 6,
          social: "Email",
          href: "mailto:brunoxbkd@gmail.com",
          iclass: "bx bx-mail-send",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../style.scss";
@import "../Squares/Squares.style.scss";
</style>
