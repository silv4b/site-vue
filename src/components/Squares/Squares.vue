<template>
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
      <div v-for="sl in socialList" v-bind:key="sl.id" :class="classCard" @click="openLink(sl.href)">
        <a :href="sl.href" target="_blank" :class="classSocialIcons">
          <i :class="sl.iclass"></i>
        </a>
      </div>
    </div>
    <!-- MODAL PLAYLISTS SPOTIFY -->
    <div class="container">
      <div type="button" @click="$refs.modalName.openModal()" class="spotify-button">
        <div class="container-row">
          <a class="social_icon_style_2">
            <i class="bx bxs-playlist"></i>
          </a>
          <div class="change_later"></div>
        </div>
      </div>
      <modal ref="modalName">
        <template v-slot:header>
          <h1>Playlists</h1>
        </template>
        <template v-slot:body>
          <div class="container font-card-color">
            <div v-for="pl in playList" v-bind:key="pl.id" class="flex left spotify-pl-card" @click="openLink(pl.link)">
              <div :class="pl.cover" :style="{ 'background-image': `url(${pl.image})` }"></div>
              <div class="spotify-pl-container">
                <div class="spotify-pl-title">{{ pl.nome }}</div>
                <div class="spotify-pl-desc">{{ pl.desc }}</div>
              </div>
            </div>
          </div>
        </template>
      </modal>
    </div>
    <!-- TEXTO E LOGO -->
    <div class="container">
      <div class="text-bottom">{{ person.desc }}</div>
      <div class="logo-img bx-tada-hover">
        <img src="@/assets/logo.svg" />
      </div>
    </div>
  </div>
</template>

<script>
import Modal from "../Modal/Modal.vue";
import Toggle from "../Toggle/Toggle.vue";
import {
  about,
  social,
  spotifyplaylists,
  imageFooter,
} from "../../../properties.js";

export default {
  components: {
    Modal,
    Toggle,
  },
  methods: {
    openLink: function (link) {
      window.open(link, "_blank");
    },
  },
  data() {
    return {
      person: about.person,
      playList: spotifyplaylists,
      socialList: social,
      imageFooter: imageFooter,
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
