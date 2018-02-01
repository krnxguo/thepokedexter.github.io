<template>
  <div id="experience">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <h3 class="display-1 section-title">{{ title }}</h3>
      </v-flex>
    </v-layout>
    <job
      v-for="(job) in experience" :key="job.employer + job.startDate"
      :employer="job.employer"
      :startDate="job.startDate"
      :endDate="job.endDate"
      :position="job.position"
      :bulletPoints="job.bulletPoints"
      :projects="job.projects"
      :skills="job.skills"
    ></job>
  </div>
</template>

<script>
import data from '../assets/data/experience'
import Job from './common/Job'

export default {
  components: { Job },
  data () {
    return {
      experience: data.experience,
      title: data.title
    }
  }
}
</script>
