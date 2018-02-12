<template>
  <v-app id="v-app">
    <!-- <navigation></navigation> -->
    <v-container grid-list-xl>
      <contact-info id="contact-info"/>
      <introduction id="introduction"/>
      <technologies id="technologies"/>
      <experience id="experience"/>
      <projects id="projects"/>
      <education id="education"/>
      <other-experience id="other-experience"/>
      <!-- <interests id="interests"/> -->
    </v-container>
  </v-app>
</template>

<script>
import ContactInfo from './components/ContactInfo'
import Introduction from './components/Introduction'
import Navigation from './components/Navigation'
import Experience from './components/Experience'
import Projects from './components/Projects'
import Technologies from './components/Technologies'
import Education from './components/Education'
import OtherExperience from './components/OtherExperience'
import Interests from './components/Interests'

export default {
  components: {
    ContactInfo,
    Introduction,
    Navigation,
    Experience,
    Projects,
    Technologies,
    Education,
    OtherExperience,
    Interests
  },
  data () {
    return {}
  }
}
</script>

<style>
#v-app {
  background-image: url('./assets/background-pattern.png');
  background-attachment: fixed;
}
#contact-info {
  margin-top: 48px;
}
</style>