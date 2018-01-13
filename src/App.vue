<template>
  <v-app id="v-app">
    <navigation></navigation>
    <v-container grid-list-xl>
      <contact-info id="first-section"/>
      <introduction/>
      <span v-for="skill in skills" :key="skill.skillType">
        <skills
          :title="skill.skillType"
          :skills="skill.skills"
        />
      </span>
    </v-container>
  </v-app>
</template>

<script>
import ContactInfo from './components/ContactInfo'
import Introduction from './components/Introduction'
import Skills from './components/Skills'
import Navigation from './components/Navigation'

import skills from './assets/data/skills'

export default {
  components: {
    ContactInfo,
    Introduction,
    Skills,
    Navigation
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
#first-section {
  margin-top: 96px;
}
</style>