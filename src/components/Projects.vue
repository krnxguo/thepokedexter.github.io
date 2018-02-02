<template>
  <div id="projects">
    <section-title :title="title"/>
    <project
      v-for="(project) in projects"
      :key="project.projectName"
      :projectName="project.projectName"
      :startDate="project.startDate"
      :endDate="project.endDate"
      :bulletPoints="project.bulletPoints"
      :technologies="project.technologies"
    />
  </div>
</template>

<script>
import data from '../assets/data/projects'

import Project from './common/Project'
import SectionTitle from './common/SectionTitle'

export default {
  components: { Project, SectionTitle },
  data () {
    return {
      title: data.title,
      projects: data.projects
    }
  }
}
</script>