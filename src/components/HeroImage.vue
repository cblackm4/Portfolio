<template>
  <v-container
    bg
    grid-list-md
    text-xs-center
    fluid
    fill-height
    class="home-hero"
  >
    <v-layout align-center justify-center wrap>
      <v-flex align-self-end xs12 md12>
        <h1 class="display-3 font-weight-thin white--text">
          Hello, My Name is Chris :D
        </h1>
        <h4 class="headline white--text">I'm a Frontend Developer!</h4>
      </v-flex>
      <v-flex pb-5 xs12 align-self-end>
        <span class="subheading white--text">Learn more about me!</span>
        <br />
        <v-btn
          onClick="document.getElementById('scrollTar').scrollIntoView({behavior: 'smooth'});"
          fab
          class="circle"
        >
          <v-icon class="expand" large color="black">expand_more</v-icon>
        </v-btn>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: "HeroImage"
};
</script>

<style scoped lang="sass">
.home-hero
    background-image: linear-gradient(rgba(0, 0, 0, 0.3),rgba(0, 0, 0, 0.3)), url("../../resources/hero-image.jpg")
    height: 100vh
    background-attachment: fixed
    background-position: center
    background-repeat: no-repeat
    background-size: cover
.circle
    color: white
    opacity: 0.6
</style>
