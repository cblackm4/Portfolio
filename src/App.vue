<template>
  <v-app>
    <navigation />

    <!-- Content -->
    <v-content id="content">
      <router-view></router-view>
    </v-content>

    <!-- Footer -->
    <v-footer></v-footer>
  </v-app>
</template>

<script>
import Navigation from "@/components/Navigation";

export default {
  name: "App",
  components: {
    Navigation
  },
  data() {
    return {};
  }
};
</script>

<style lang="sass"></style>
