<template>
  <v-app id="v-app">
    <navigation></navigation>
    <v-container grid-list-xl>
      <contact-info id="contact-info"/>
      <introduction id="introduction"/>
      <technologies id="technologies"/>
      <tools id="tools"/>
      <experience id="experience"/>
      <projects id="projects"/>
    </v-container>
  </v-app>
</template>

<script>
import ContactInfo from './components/ContactInfo'
import Introduction from './components/Introduction'
import Navigation from './components/Navigation'
import Tools from './components/Tools'
import Experience from './components/Experience'
import Projects from './components/Projects'
import Technologies from './components/Technologies'

export default {
  components: {
    ContactInfo,
    Introduction,
    Navigation,
    Tools,
    Experience,
    Projects,
    Technologies
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
  margin-top: 96px;
}
</style>