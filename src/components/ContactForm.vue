<template>
  <v-card flat>
    <v-form class="form">
      <v-text-field prepend-icon="person" label="First Name"></v-text-field>

      <v-text-field prepend-icon="person" label="Last Name"></v-text-field>

      <v-text-field prepend-icon="email" label="Business E-mail"></v-text-field>

      <v-text-field prepend-icon="business" label="Company"></v-text-field>
      <v-text-field prepend-icon="phone" label="Phone Number"></v-text-field>
      <v-select
        prepend-icon="navigation"
        label="State"
        :items="states_us"
      ></v-select>
      <v-select
        prepend-icon="short_text"
        label="Reason for Contact"
        :items="con_reasons"
      ></v-select>
      <v-textarea
        prepend-icon="message"
        rows="5"
        no-resize
        label="Additional Information"
      ></v-textarea>
      <v-btn color="success">Submit</v-btn>
    </v-form>
  </v-card>
</template>

<script>
export default {
  name: "ContactForm",
  data: () => ({
    states_us: [
      "AK",
      "AL",
      "AR",
      "AZ",
      "CA",
      "CO",
      "CT",
      "DE",
      "FL",
      "GA",
      "HI",
      "IA",
      "ID",
      "IL",
      "IN",
      "KS",
      "KY",
      "LA",
      "MA",
      "MD",
      "ME",
      "MI",
      "MN",
      "MO",
      "MS",
      "MT",
      "NC",
      "ND",
      "NE",
      "NH",
      "NJ",
      "NM",
      "NV",
      "NY",
      "OH",
      "OK",
      "OR",
      "PA",
      "RI",
      "SC",
      "SD",
      "TN",
      "TX",
      "UT",
      "VA",
      "VT",
      "WA",
      "WI",
      "WV",
      "WY"
    ],
    con_reasons: ["Recruitment", "Contract Work", "Pricing", "Support"]
  })
};
</script>

<style>
.form {
}
</style>
