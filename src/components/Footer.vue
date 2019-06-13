<template>
  <v-footer class="foot-main" height="250" color="#707070">
    <v-layout justify-center wrap>
      <v-flex
        v-for="info in infos"
        :key="info"
        py-3
        text-xs-center
        white--text
        xs4
        md2
        >{{ info }}</v-flex
      >
      <v-flex xs12 md12 text-xs-center>
        <v-btn
          class="mx-3 foot-links"
          v-for="social in socials"
          :key="social"
          fab
          light
        >
          <v-icon size="24px">{{ social }}</v-icon>
        </v-btn>
      </v-flex>
      <v-flex py-3 text-xs-center white--text xs12>
        &copy;2019 —
        <strong>Christopher Blackmon</strong>
      </v-flex>
    </v-layout>
  </v-footer>
</template>

<script>
export default {
  name: "Footer",
  data: () => ({
    socials: [
      "fab fa-facebook",
      "fab fa-twitter",
      "fab fa-github",
      "fab fa-linkedin",
      "fab fa-stack-overflow"
    ],
    infos: ["(803) 468-8787", "blackmonc21@gmail.com", "Columbia, SC"]
  })
};
</script>

<style scoped lang="sass">
.foot-main
    background-color: #707070
    color: white
.foot-links
    color: #707070
.foot-links:hover
    color: black
</style>
