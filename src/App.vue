<template>
  <v-app id="v-app">
    <v-container grid-list-xl>
      <contact-info/>
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

import skills from './assets/data/skills'

export default {
  components: {
    ContactInfo,
    Introduction,
    Skills
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
</style>