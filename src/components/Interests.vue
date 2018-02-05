<template>
  <div id="interests">
    <section-title :title="title"/>
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card dark color="deep-orange">
          <v-container>
            hello
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import data from '../assets/data/interests'

import SectionTitle from './common/SectionTitle'

export default {
  components: { SectionTitle },
  data () {
    return {
      title: data.title,
      interests: data.interests
    }
  }
}
</script>

<style>

</style>
