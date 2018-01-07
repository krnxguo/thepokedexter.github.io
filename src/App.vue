<template>
  <v-app id="v-app">
    <v-container grid-list-xl>
      <contact-info/>
      <introduction/>
      <skills/>
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
    return {}
  }
}
</script>

<style>
#v-app {
  background-image: url('./assets/gplaypattern.png');
  background-attachment: fixed;
}
</style>