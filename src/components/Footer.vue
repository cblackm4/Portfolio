<template>
  <v-footer class="foot-main" height="250" color="#707070">
    <v-layout justify-center wrap>
      <v-flex
        v-for="(info, i) in infos"
        :key="i"
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
          v-for="(social, i) in socials"
          :key="i"
          fab
          light
          depressed
          :href="social.url"
          :target="social.target"
        >
          <a>
            <v-icon size="24px">{{ social.icon }}</v-icon>
          </a>
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
      { icon: "fab fa-facebook", url: "http://facebook.com", target: "_blank" },
      {
        icon: "fab fa-twitter",
        url: "https://twitter.com/blackmonc21",
        target: "_blank"
      },
      {
        icon: "fab fa-github",
        url: "https://github.com/cblackm4",
        target: "_blank"
      },
      {
        icon: "fab fa-linkedin",
        url: "https://www.linkedin.com/in/christopherjblackmon/",
        target: "_blank"
      },
      {
        icon: "fab fa-stack-overflow",
        url:
          "https://stackoverflow.com/users/5009042/chris-blackmon?tab=profile",
        target: "_blank"
      }
    ],
    infos: ["(803) 468-8787", "blackmonc21@gmail.com", "Columbia, SC"]
  })
};
</script>

<style scoped lang="sass">
.foot-main
    background-color: #707070
    color: white
.foot-links a
    color: #707070
.foot-links:hover a
    color: black
</style>
