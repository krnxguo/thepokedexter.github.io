<template>
  <div id="other experience">
    <section-title :title="title"/>
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card>
          <v-toolbar class="purple" dense dark flat>
            <v-toolbar-title>{{ experience.employer }}</v-toolbar-title>
          </v-toolbar>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import data from '../assets/data/other-experience'

import SectionTitle from './common/SectionTitle'

export default {
  components: { SectionTitle },
  data () {
    return {
      title: data.title,
      experience: data.experience
    }
  }
}
</script>

<style>

</style>
