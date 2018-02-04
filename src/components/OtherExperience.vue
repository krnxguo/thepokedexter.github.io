<template>
  <div id="other experience">
    <section-title :title="title"/>
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card>
          <v-toolbar class="purple" dense dark flat>
            <v-toolbar-title>{{ experience.employer }}</v-toolbar-title>
          </v-toolbar>
          <v-container>
            <h5 class="headline">{{ experience.position }}</h5>
            <h6
              v-for="(date) in experience.employmentDates"
              :key="date.startDate + date.endDate"
              class="title employment-date"
            >
              {{ date.startDate + ' - ' + date.endDate }}
            </h6>
          </v-container>
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
.employment-date {
  margin-bottom: 6px;
  margin-left: 12px;
  font-weight: 400;
}
</style>
