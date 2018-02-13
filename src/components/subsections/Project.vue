<template>
  <div id="project">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card>
          <v-toolbar class="indigo" dense dark flat>
            <v-spacer></v-spacer>
            <v-toolbar-title>{{ startDate + " - " + endDate }}</v-toolbar-title>
          </v-toolbar>
          <v-container>
            <h5 class="headline project-name">{{ projectName }}</h5>
            <ul v-if="bulletPoints.length > 0">
              <li v-for="(bulletPoint, index) in bulletPoints" :key="projectName + index">
                <span class="body-1">{{ bulletPoint }}</span>            
              </li>
            </ul>
            <technologies-used :technologies="technologies"/>
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
    projectName: {
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
    bulletPoints: {
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
.project-name {
  margin-top: 8px;
  margin-bottom: 16px;
}
</style>
