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

      <!-- PLAYLIST SPOTIFY 
      <div class="container">
        <div type="button" @click="spotifyLink()" class="spotify-button">
          <div class="container-row">
            <a class="social_icon_style_2"><i class="bx bxl-spotify"></i> </a>
          </div>
        </div>
      </div> -->

      <!-- MODAL PLAYLISTS SPOTIFY -->
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
            <div class="container a90">
              <div @click="spotifyLink1()" class="flex left spotify-pl-card">
                <div class="card-pl-art"></div>
                <div class="spotify-pl-container">
                  <div class="spotify-pl-title">🎵 Songs to not be sad</div>
                  <div class="spotify-pl-desc">
                    Uma playlist bem aleatória pra você curtir sem medo de ser
                    feliz, variando desde de rap até theme songs de animes.
                  </div>
                </div>
              </div>
              <div @click="spotifyLink2()" class="flex left spotify-pl-card">
                <div class="card-pl-art2"></div>
                <div class="spotify-pl-container">
                  <div class="spotify-pl-title">🎶 Songs to not be sad 2.0</div>
                  <div class="spotify-pl-desc">
                    Versão 2.0 da playlist anterior, mais aleatória, mas
                    interessante, só vai!
                  </div>
                </div>
              </div>
            </div>
          </template>
        </modal>
      </div>

      <!-- TEXTO E LOGO -->
      <div class="container">
        <div class="text-bottom">{{ texts[2] }}</div>
        <div class="logo-img">
          <img src="@/assets/logo.svg" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Modal from "../Modal/Modal.vue";
//import * as Square from "./Squares";

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
    spotifyLink1: function () {
      window.open(this.playlists[0].link, "_blank");
    },
    spotifyLink2: function () {
      window.open(this.playlists[1].link, "_blank");
    },
  },
  data() {
    return {
      imageFooter:
        "https://raw.githubusercontent.com/silv4b/site-vue/5f3230901f5a602e3b69ef8c81c3fd30b9109f5a/src/assets/logo.svg?token=AEJJ7YUABF7DUNQZ2LMALI3A5QZTO",
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
      playlists: [
        {
          id: 1,
          nome: "🎵 Songs to not be sad",
          link: "https://open.spotify.com/playlist/1sBicr7fa2fbPJlBNq6hCX",
          image:
            "https://i.scdn.co/image/ab67706c0000bebb86aa1b28e2f2d22a9811222b",
        },
        {
          id: 2,
          nome: "🎶 Songs to not be sad 2.0",
          link: "https://open.spotify.com/playlist/7FCrKytZs7U3Mm4WXWabVm",
          image:
            "https://i.scdn.co/image/ab67706c0000bebb7490f9f68e3766e57c6fd4e3",
        },
      ],
      playlistsImage: [
        "https://i.scdn.co/image/ab67706c0000bebb7490f9f68e3766e57c6fd4e3",
        "https://i.scdn.co/image/ab67706c0000bebb86aa1b28e2f2d22a9811222b",
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../../style.scss";
@import "../../style.breakpoints.scss";
@import "../Squares/Squares.style.scss";
@import "../Modal/Modal.style.scss";

.a90 {
  color: whitesmoke;
  font-weight: 200;
  display: flex;
}

.spotify-pl-card {
  height: 200px;
  width: 520px;
  border-radius: 6px;
  margin-bottom: 30px;
  background: $full-background-color;
  transition: 0.2s ease-in-out;
  cursor: pointer;
}

.spotify-pl-card:hover {
  transform: scale(1.04);
}

.spotify-pl-container {
  max-width: 450px;
  height: auto;
  padding: 20px 0;
}

.spotify-pl-title {
  font-weight: 400 !important;
  font-size: 1.2rem;
  text-align: left;
}

.spotify-pl-desc {
  margin-top: 16px;
  font-weight: 200 !important;
  font-size: 0.8rem;
  width: 260px;
  text-align: left;
}

.card-pl-art {
  height: 200px;
  width: 200px;
  background: $white-color;
  margin-right: 30px;
  border-radius: 6px 0 0 6px;
  background: url(https://i.scdn.co/image/ab67706c0000bebb86aa1b28e2f2d22a9811222b);
  background-size: 202px 202px;
  background-position: center;
}

.card-pl-art2 {
  height: 200px;
  width: 200px;
  background: $white-color;
  margin-right: 30px;
  border-radius: 6px 0 0 6px;
  background: url(https://i.scdn.co/image/ab67706c0000bebb7490f9f68e3766e57c6fd4e3);
  background-size: 202px 202px;
  background-position: center;
}
</style>
