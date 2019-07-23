<template>
  <v-container id="scrollTar" grid-list-md text-xs-center fluid>
    <!--Section 1-->
    <v-layout pt-5 pb-5 justify-center row wrap>
      <v-flex xs12 align-self-center>
        <h4 class="display-1 section-header">What I'm About</h4>
      </v-flex>
      <v-flex xs12 md3 v-for="(card, i) in cards" :key="i">
        <v-card flat>
          <v-card-title class="justify-center headline section-header">
            {{ card.title }}
          </v-card-title>
          <v-icon size="75">{{ card.icon }}</v-icon>
          <v-card-text class="text-xs-left">{{ card.text }}</v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
    <!--Section 2-->
    <v-layout pb-5 justify-center row wrap>
      <v-flex row wrap align-self-center xs12>
        <h4 class="display-1 section-header">What I Use</h4>
      </v-flex>
      <!--eslint throws error but this code is valid src: https://github.com/vuejs/vetur/issues/261-->
      <v-flex
        xs12
        md12
        v-bind:key="devicon"
        v-for="(devicon, i) in Math.ceil(devicons.length / 3)"
      >
        <!--eslint throws error but this code is valid src: https://github.com/vuejs/vetur/issues/261-->
        <v-icon
          v-bind:key="devicon"
          v-for="devicon in devicons.slice(i * 3, (i + 1) * 3)"
          >{{ devicon }}</v-icon
        >
      </v-flex>
    </v-layout>
    <!--Section 3-->
    <v-layout pb-5 justify-center row wrap>
      <v-flex xs12 align-self-center>
        <h4 class="display-1 section-header">What I've Built</h4>
      </v-flex>
      <v-flex xs12 sm12 md5 v-for="(website, i) in websites" :key="i">
        <v-card height="100%">
          <v-parallax class="site-parallax" :src="website.image"></v-parallax>
          <v-card-title primary-title>
            <div>
              <div class="headline">{{ website.name }}</div>
              <div class="text-xs-left">{{ website.about }}</div>
            </div>
          </v-card-title>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn
              class="subhead-btn"
              color="#707070"
              :href="website.url"
              :target="website.target"
              >Visit</v-btn
            >
            <v-btn
              class="subhead-btn"
              color="#707070"
              :href="website.source"
              :target="website.target"
            >
              <v-icon>fab fa-github</v-icon>
              <span class="btn-text">Source</span>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: "HomeContent",
  data: () => ({
    cards: [
      {
        title: "Development",
        icon: "code",
        text:
          "I graduated with distinction from my Computer Science program. You can bet I'm serious about development! Developing web applications make others lives easier - customers and business owners alike!"
      },
      {
        title: "The Customer",
        icon: "people",
        text:
          "My experience as a customer service representative taught me how tovalue the customer and put their needs first, no matter theobstacle. I apply this same attitude towards my work as a webdeveloper - my main goal is always client satisfaction!"
      },
      {
        title: "Design",
        icon: "web",
        text:
          "I love being creative and designing new things - especially websites! My approach is always to create the most professional and clean UI/UX experience, so that the audience has no trouble getting the information they need, when they need it."
      }
    ],
    websites: [
      {
        name: "The Ashanti Foundation",
        image: require("../../resources/ashanti.jpg"),
        url: "https://cblackm4.github.io/Ashanti-Foundation/",
        source: "https://github.com/cblackm4/Ashanti-Foundation",
        target: "_blank",
        about:
          "The Ashanti Foundation website is dedicated to the memory of Ashanti Billie as well as being a portal for The Ashanti Foundation itself. The foundation works in the community to help families and individuals in the event of adult abductions."
      },
      {
        name: "Pawkages",
        image: require("../../resources/paw.jpg"),
        url: "https://pawkages.herokuapp.com/accounts/login/",
        source: "https://github.com/cblackm4/ecommerceproject",
        target: "_blank",
        about:
          "Pawkages is a fictional e-commerce animal food mart created with Vue.js built to display my skills in building app features. My work was focused on the design of the website and the subscriptions feature while also providing support to my teammates in other areas throughout development."
      }
    ],
    devicons: [
      "devicon-html5-plain-wordmark colored",
      "devicon-css3-plain-wordmark colored",
      "devicon-javascript-plain colored",
      "devicon-vuejs-plain-wordmark colored",
      "devicon-sass-original colored",
      "devicon-github-plain-wordmark colored"
    ]
  })
};
</script>
<style scoped lang="sass">

.devicon-html5-plain-wordmark, .devicon-css3-plain-wordmark, .devicon-javascript-plain, .devicon-vuejs-plain-wordmark, .devicon-sass-original, .devicon-github-plain-wordmark
    font-size: 8em
    padding: .3em

.site-parallax
    opacity: 0.9
    transition: opacity .5s ease-out
    -moz-transition: opacity .5s ease-out
    -webkit-transition: opacity .5s ease-out
    -o-transition: opacity .5s ease-out

.site-parallax:hover
    opacity: 1

.subhead-btn
    color: white

.btn-text
    padding-left: .5em
</style>
