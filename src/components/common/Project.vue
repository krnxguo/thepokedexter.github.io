<template>
  <div id="project">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card>
          <v-toolbar class="indigo" dense dark flat>
            <v-spacer></v-spacer>
            <v-toolbar-title>{{ startDate + " - " + endDate}}</v-toolbar-title>
          </v-toolbar>
          <v-container>
            <h5 class="headline project-name">{{ projectName }}</h5>
            <ul v-if="bulletPoints.length > 0">
              <li v-for="(bulletPoint, index) in bulletPoints" :key="projectName + index">
                <span class="body-1">{{ bulletPoint }}</span>            
              </li>
            </ul>
            <span v-if="skills.length > 0">
              <hr/>
              <h6 class="technologies-used-title">Technologies Used</h6>
              <div class="technologies">
                <v-chip v-for="(skill) in skills" :key="skill">
                  <strong>{{ skill }}</strong>
                </v-chip>
              </div>
            </span>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {
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
    skills: {
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
.technologies-used-title {
  margin: 16px 0 12px 5px;
  font-size: 15px;
  font-weight: 500;
  text-transform: uppercase;
}
.technologies {
  margin-bottom: 8px;
}
</style>
