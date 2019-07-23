<template>
  <v-app>
    <link
      rel="stylesheet"
      href="https://cdn.rawgit.com/konpa/devicon/df6431e323547add1b4cf45992913f15286456d3/devicon.min.css"
    />
    <link
      href="https://use.fontawesome.com/releases/v5.0.13/css/all.css"
      rel="stylesheet"
    />
    <navigation />
    <!-- Content -->
    <v-content id="content">
      <router-view></router-view>
    </v-content>
    <foot></foot>

    <!-- Footer -->
  </v-app>
</template>

<script>
import Navigation from "@/components/Navigation";
import Foot from "@/components/Footer";

export default {
  name: "App",
  components: {
    Navigation,
    Foot
  },
  data() {
    return {};
  }
};
</script>

<style lang="sass">
.section-header
    color: #707070
.content-header
    position: absolute
    color: white
    top: 50%
    left: 0
    right: 0
    transform: translate(0, -50%)
    text-align: center
.theme--light.application
  background-color: #fff
</style>
