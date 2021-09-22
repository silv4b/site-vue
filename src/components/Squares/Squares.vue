<template>
  <div class="master-border">
    <div class="container">
      <!-- TOGGLE -->
      <div class="container toggle">
        <Toggle />
      </div>
      <!--  PERFIL -->
      <div class="container">
        <div class="profile"></div>
      </div>

      <!-- TEXTOS -->
      <div class="container">
        <div class="text-name">{{ person.title }}</div>
        <div class="text-job">{{ person.job }}</div>
      </div>

      <!-- REDES SOCIAIS -->
      <div class="container-row">
        <div
          v-for="sl in socialList"
          v-bind:key="sl.id"
          :class="classCard"
          @click="openLinkDiv(sl.href)"
        >
          <a :href="sl.href" target="_blank" :class="classSocialIcons">
            <i :class="sl.iclass"></i>
          </a>
        </div>
      </div>

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
            <div class="container font-card-color">
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
        <div class="text-bottom">{{ person.desc }}</div>
        <div class="logo-img">
          <img src="@/assets/logo.svg" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Modal from "../Modal/Modal.vue";
import Toggle from "../Toggle/Toggle.vue";
import {
  about,
  newSocialList,
  social,
  playlist,
  imageFooter,
} from "../../../properties.js";

export default {
  components: {
    Modal,
    Toggle,
    /* eslint-disable vue/no-unused-components */
    about,
    newSocialList,
    social,
    playlist,
    imageFooter,
  },
  methods: {
    spotifyLink1: function () {
      window.open(this.playlists[0].link, "_blank");
    },
    spotifyLink2: function () {
      window.open(this.playlists[1].link, "_blank");
    },
    openLinkDiv: function (link) {
      window.open(link, "_blank");
    },
  },
  data() {
    return {
      person: about.person,
      socialList: social,
      imageFooter: imageFooter,
      playlists: playlist,
      classCard: "social center",
      classSocialIcons: "social_icon_style",
    };
  },
};
</script>

<style lang="scss">
@import "../../style.scss";
@import "../../style.breakpoints.scss";
@import "../Squares/Squares.style.scss";
@import "../Modal/Modal.style.scss";
</style>
