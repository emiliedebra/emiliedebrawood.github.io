<!-- Education Page -->

<template>
  <v-container flat text-xs-left class="education-page width-limit-500">
    <h3 class="head">Tertiary Education</h3>
    <education-text v-for="item in tertiary" :key="item.title" :content="item"></education-text>
    <v-container class="divider-container" pa-0 pt-3 pb-3>
      <v-divider></v-divider>
    </v-container>
    <h3 class="head">Secondary Education</h3>
    <education-text v-for="item in secondary" :key="item.title" :content="item"></education-text>
  </v-container>
</template>

<script>
import EducationText from "../components/text/EducationText.vue";

export default {
  name: "education",
  data() {
    return {
      tertiary: [
        {
          institution: "University of Cape Town",
          year: "July 2017 - November 2017",
          description: "BSc in Computer Science and Computer Engineering",
          additional: "Graduated with a 76.5% average",
          logo: "logo"
        },
        {
          institution: "University of Cape Town",
          year: "2015 – July 2017",
          description: "BSc Eng in Electrical and Computer Engineering",
          additional: "Dean's Merit List Student for 2015, 2016 and 2017",
          logo: "Port_Shepstone_High_School.gif"
        }
      ],
      secondary: [
        {
          institution: "Port Shepstone High School",
          year: "2010 - 2014",
          description: "National Senior Certificate",
          additional: "Awarded Dux of the School"
        }
      ]
    };
  },
  components: {
    EducationText
  }
};
</script>
<style>
.education-page {
  padding-top: 0;
  padding-bottom: 0;
}
</style>
