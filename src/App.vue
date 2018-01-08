<template>
  <v-app id="v-app">
    <v-container grid-list-xl>
      <contact-info/>
      <introduction/>
      <skills
        title="Programming Languages"
        :skills="programmingLanguages"
      />
    </v-container>
  </v-app>
</template>

<script>
import ContactInfo from './components/ContactInfo'
import Introduction from './components/Introduction'
import Skills from './components/Skills'

export default {
  components: {
    ContactInfo,
    Introduction,
    Skills
  },
  data () {
    return {
      programmingLanguages: [
        {label: 'Javascript', rating: 5},
        {label: 'Typescript', rating: 5},
        {label: 'HTML/CSS', rating: 5},
        {label: 'C#', rating: 3},
        {label: 'C++', rating: 3},
        {label: 'Python', rating: 2}
      ]
    }
  }
}
</script>

<style>
#v-app {
  background-image: url('./assets/gplaypattern.png');
  background-attachment: fixed;
}
</style>