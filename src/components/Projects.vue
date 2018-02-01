<template>
  <div id="projects">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <h3 class="display-1 section-title">{{ title }}</h3>
      </v-flex>
    </v-layout>
    <project
      v-for="(project) in projects"
      :key="project.projectName"
      :projectName="project.projectName"
      :startDate="project.startDate"
      :endDate="project.endDate"
      :bulletPoints="project.bulletPoints"
      :skills="project.skills"
    />
  </div>
</template>

<script>
import data from '../assets/data/projects'
import Project from './common/Project'

export default {
  components: { Project },
  data () {
    return {
      title: data.title,
      projects: data.projects
    }
  }
}
</script>