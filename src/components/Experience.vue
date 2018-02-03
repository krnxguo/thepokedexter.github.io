<template>
  <div id="experience">
    <section-title :title="title"/>
    <job
      v-for="(job) in experience" 
      :key="job.employer + job.startDate"
      :employer="job.employer"
      :startDate="job.startDate"
      :endDate="job.endDate"
      :position="job.position"
      :bulletPoints="job.bulletPoints"
      :projects="job.projects"
      :technologies="job.technologies"
    ></job>
  </div>
</template>

<script>
import data from '../assets/data/experience'
import Job from './subsections/Job'
import SectionTitle from './common/SectionTitle'

export default {
  components: { Job, SectionTitle },
  data () {
    return {
      experience: data.experience,
      title: data.title
    }
  }
}
</script>
