<template>
  <v-app id="v-app">
    <v-container grid-list-xl>
      <contact-info></contact-info>
      <introduction></introduction>
    </v-container>
  </v-app>
</template>

<script>
import ContactInfo from './components/ContactInfo'
import Introduction from './components/Introduction'

export default {
  components: {
    ContactInfo,
    Introduction
  },
  data () {
    return {
    }
  }
}
</script>

<style>
#v-app {
  background-image: url('./assets/gplaypattern.png');
}
</style>