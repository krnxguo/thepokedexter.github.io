<template>
  <div id="job">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card>
          <v-toolbar class="light-blue" dark flat>
            <v-toolbar-title>{{ employer }}</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-toolbar-title>{{ startDate + " - " + endDate}}</v-toolbar-title>
          </v-toolbar>
          <v-container>
            <h5 class="headline position">{{ position }}</h5>
            <ul v-if="bulletPoints.length > 0">
              <li v-for="(bulletPoint, index) in bulletPoints" :key="position + index">
                <span class="body-1">{{ bulletPoint }}</span>            
              </li>
            </ul>
            <span 
              v-if="projects.length > 0"
              v-for="(project) in projects" 
              :key="project.projectName" 
            >
              <h6 class="title project-name">{{ project.projectName }}</h6>
              <ul v-if="project.bulletPoints.length > 0">
                <li 
                  v-for="(projectBulletPoint, index) in project.bulletPoints" 
                  :key="project.projectName + index"
                >
                  <span class="body-1">{{ projectBulletPoint }}</span>            
                </li>
              </ul>
            </span>
            <technologies-used :technologies="technologies" />
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import TechnologiesUsed from '../common/TechnologiesUsed'

export default {
  components: { TechnologiesUsed },
  props: {
    employer: {
      type: String,
      required: true
    },
    startDate: {
      type: String,
      required: true
    },
    endDate: {
      type: String,
      required: true
    },
    position: {
      type: String,
      required: true
    },
    bulletPoints: {
      type: Array,
      default: function () {
        return []
      }
    },
    projects: {
      type: Array,
      default: function () {
        return []
      }
    },
    technologies: {
      type: Array,
      default: function () {
        return []
      }
    }
  },
  data () {
    return {}
  }
}
</script>

<style>
.position, .project-name {
  margin-top: 8px;
  margin-bottom: 16px;
}
</style>