<template>
  <v-app>
    <v-container grid-list-xl>
      <contact-info></contact-info>
    </v-container>
  </v-app>
</template>

<script>
import ContactInfo from './components/ContactInfo'

export default {
  components: {ContactInfo},
  data () {
    return {
    }
  }
}
</script>
