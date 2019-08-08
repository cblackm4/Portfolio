<template>
  <v-container
    id="about-section"
    class="alt-section"
    grid-list-md
    text-xs-center
    fluid
  >
    <v-layout pt-5 pb-5 justify-center row wrap>
      <v-flex xs12 align-self-center>
        <h4 class="display-1 alt-section-header">About Me</h4>
      </v-flex>

      <v-flex xs12 sm12 md4 pa-2>
        <v-img xs5 :src="images.about" height="525"></v-img>
      </v-flex>
      <v-flex xs12 md4 pa-2 class="text-xs-left">
        <p>
          Growing up, I was always infuated with technology. Whether it be
          playing video games, taking apart an electronic and learning about the
          internet - it's always been a passion of mine. As a teenager, my
          interest in technology grew and took me to creating fan websites of my
          favorite hobbies. It was at this time that I unknowingly planted the
          seeds for my professional life.
        </p>
        <p>
          Fast forward to 2014. I had just become a father and I was looking for
          a career change. This led me to Central Carolina Technical College,
          where I enrolled in the school's Computer Technology program. It was
          here that I was able to begin honing my fundamentals of programming
          using languages like Java, C# and SQL. Upon graduating with a 3.4 GPA
          in 2016, I knew I wanted to further my formal education. I decided to
          enroll in the University of Maryland University College (now known as
          University of Maryland Global Campus). From here, I pursued my
          Bachelor's Degree in Computer Sceience. I also begun to take Web
          Development elective classes and re-ignited my passion for Web
          Development. Combining my previous experience as a teenager in the web
          with my newfound skills in traditional programming, I was able to jump
          start my path to becoming the best web developer I can be. I graduated
          Cum Laude from UMUC with a 4.86 GPA in 2019.
        </p>
        <p>
          Today, I currently work as an Associate Frontend Developer at Unum. My
          speciality in web development is my combination of strong programming
          fundamentals in JavaScript and my eye for professional and realistic
          design that provides an excellent user experience. This portfolio
          serves as my home for implementing new techniques and ideas, as well
          as sharing my journey with prospective employers, colleagues and
          followers.
        </p>
        <p>Thank you for visiting!</p>
        <p>Christopher Blackmon</p>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    images: {
      about: require("../../resources/about-img.jpg")
    }
  })
};
</script>

<style scoped lang="sass"></style>
