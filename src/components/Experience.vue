<template>
  <div id="experience">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <h3 id="title" class="display-2">{{ title }}</h3>
        <job
          v-for="(job) in experience" :key="job.employer + job.startDate"
          :employer="job.employer"
          :startDate="job.startDate"
          :endDate="job.endDate"
          :position="job.position"
        ></job>
      </v-flex>
    </v-layout>
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

<style>
#title {
  text-align: center;
  color: #494949;
  margin-top: 1.5rem;
  margin-bottom: 1.5rem;
}
</style>