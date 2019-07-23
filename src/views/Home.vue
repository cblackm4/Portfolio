<template>
  <span id="top">
    <hero-image />
    <home-content />
    <about-content />
    <contact-content />
  </span>
</template>

<script>
import HeroImage from "@/components/HeroImage";
import HomeContent from "@/components/HomeContent";
import AboutContent from "@/components/AboutContent";
import ContactContent from "@/components/ContactContent";
export default {
  components: {
    HeroImage,
    HomeContent,
    AboutContent,
    ContactContent
  }
};
</script>

<style lang="sass">
.alt-section
  background-color: #707070
  color: #D1D1D1

.alt-section-header
  color: white
</style>
