<template>
  <span>
    <!-- Mobile Nav -->
    <v-navigation-drawer v-model="hamburger" app temporary>
      <v-list class="pt-0">
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
    <v-toolbar app flat>
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
          flat
          v-for="navlink in navlinks"
          :key="navlink.title"
          :to="navlink.route"
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
export default {
  name: "Navigation",
  data() {
    return {
      hamburger: false,
      navlinks: [
        { title: "Home", route: "/" },
        { title: "Projects", route: "../projects" },
        { title: "Services", route: "../services" },
        { title: "About", route: "../about" },
        { title: "Contact", route: "../contact" }
      ]
    };
  }
};
</script>

<style></style>
