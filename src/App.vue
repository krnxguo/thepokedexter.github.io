<template>
  <v-app id="v-app">
    <navigation></navigation>
    <v-container grid-list-xl>
      <contact-info id="contact-info"/>
      <introduction id="introduction"/>
      <span id="skills" v-for="skill in skills" :key="skill.skillType">
        <skills
          :title="skill.skillType"
          :skills="skill.skills"
        />
      </span>
      <tools id="tools"/>
      <experience id="experience"/>
      <projects id="projects"/>
    </v-container>
  </v-app>
</template>

<script>
import ContactInfo from './components/ContactInfo'
import Introduction from './components/Introduction'
import Skills from './components/Skills'
import Navigation from './components/Navigation'
import Tools from './components/Tools'
import Experience from './components/Experience'
import Projects from './components/Projects'

import skills from './assets/data/skills'

export default {
  components: {
    ContactInfo,
    Introduction,
    Skills,
    Navigation,
    Tools,
    Experience,
    Projects
  },
  data () {
    return {
      skills: skills
    }
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