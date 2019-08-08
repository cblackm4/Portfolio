<template>
  <span>
    <!-- Mobile Nav -->
    <v-navigation-drawer v-model="hamburger" color="white" app temporary right>
      <v-list>
        <v-divider></v-divider>
        <v-list-tile
          v-for="navlink in navlinks"
          :key="navlink.title"
          avatar
          :to="navlink.route"
        >
          <v-list-tile-content>
            <v-list-tile-title>{{ navlink.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>

    <!-- Desktop Nav -->
    <v-toolbar class="head-main" fixed flat>
      <v-avatar size="45">
        <img src="../../resources/avatar.jpg" alt="alt" />
      </v-avatar>
      <v-toolbar-title class="headline text-uppercase">
        <span class="font-weight-light">Christopher</span>
        <span class="font-weight-bold">Blackmon</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <!-- Nav -->
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn
          class="head-links"
          flat
          v-for="navlink in navlinks"
          :key="navlink.title"
          v-on:click="navHelper(navlink.target)"
          >{{ navlink.title }}</v-btn
        >
      </v-toolbar-items>

      <!-- Hamburger -->
      <v-toolbar-side-icon
        class="hidden-md-and-up"
        @click.stop="hamburger = !hamburger"
      ></v-toolbar-side-icon>
    </v-toolbar>
  </span>
</template>

<script>
$(function() {
  $(document).scroll(function() {
    var $nav = $(".head-main");
    $nav.toggleClass("scrolled", $(this).scrollTop() > $nav.height());
  });
});

export default {
  name: "Navigation",
  data() {
    return {
      hamburger: false,
      navlinks: [
        { title: "Home", target: "top" },
        { title: "About", target: "about-section" },
        { title: "Contact", target: "contact-section" }
      ]
    };
  },
  methods: {
    navHelper: function(target) {
      document.getElementById(target).scrollIntoView({ behavior: "smooth" });
    }
  }
};
</script>

<style scoped lang="sass">
.head-main
    background-color: transparent
    color: white
.head-main.scrolled
    background-color: #707070
    color: #D1D1D1
.head-links
    color: #D1D1D1
.v-btn .v-btn__content .v-icon
    color: #D1D1D1
</style>
