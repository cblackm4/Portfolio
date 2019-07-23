<template>
  <v-container id="contact-section" grid-list-md text-xs-center fluid>
    <v-layout pt-5 pb-5 justify-center row wrap>
      <v-flex xs12 align-self-center>
        <h4 class="display-1 section-header">Contact</h4>
      </v-flex>
      <v-flex id="left-contact" xs12 sm12 md4>
        <v-card flat>
          <v-card-title>
            <h1 class="heading font-weight-thin">Direct Contact</h1>
          </v-card-title>
          <v-layout pa-3 ma-0 row wrap>
            <v-flex xs12 v-for="(contact, i) in contacts" :key="i">
              <div class="con-icon text-xs-left">
                <v-icon size="52">{{ contact.icon }}</v-icon>
              </div>
              <div class="con-content text-xs-left">
                <h2>{{ contact.title }}</h2>
                <span v-html="contact.content"></span>
              </div>
            </v-flex>
          </v-layout>
          <v-card-text class="text-xs-left">
            Interested in hiring me? Have a question or suggestion? You can find
            me easily online at these social media websites:
          </v-card-text>
          <v-btn
            v-for="(con_icon, i) in con_icons"
            :key="i"
            flat
            fab
            large
            :href="con_icon.url"
            :target="con_icon.target"
          >
            <a>
              <v-icon :color="con_icon.color" size="48px">
                {{ con_icon.icon }}
              </v-icon>
            </a>
          </v-btn>
        </v-card>
      </v-flex>
      <v-flex md4>
        <v-card transparent flat>
          <v-card-title>
            <h1 class="heading font-weight-thin">Support</h1>
          </v-card-title>
          <contact-form />
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import ContactForm from "@/components/ContactForm";

export default {
  name: "ContactContent",
  components: {
    ContactForm
  },
  data: () => ({
    con_icons: [
      {
        icon: "fab fa-facebook",
        color: "#3b5998",
        url: "http://facebook.com",
        target: "_blank"
      },
      {
        icon: "fab fa-linkedin",
        color: "#0077B5",
        url: "https://www.linkedin.com/in/christopherjblackmon/",
        target: "_blank"
      }
    ],
    contacts: [
      {
        icon: "ring_volume",
        title: "Phone",
        content: "1+803-468-8787"
      },
      {
        icon: "alternate_email",
        title: "E-Mail",
        content:
          '<a href="mailto:blackmonc21@gmail.com">blackmonc21@gmail.com</a>'
      },
      {
        icon: "map",
        title: "Address",
        content: "3430 Broad River Road<br>Apartment 507<br>Columbia, SC 29210"
      }
    ]
  })
};
</script>

<style lang="sass">
.con-icon
  float: left
  margin-bottom: 3em
  padding-right: 1em
</style>
