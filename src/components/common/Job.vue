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
            <ul>
              <li>
                <span class="subheading">Designed and implemented a C++ program to manipulate MRIs for analysis</span>            
              </li>
            </ul>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {
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
    }
  },
  data () {
    return {}
  }
}
</script>

<style>
ul {
  padding-left: 20px;
}
li {
  margin: 0 0 0.5em;
}
.position {
  margin-bottom: 20px;
}
</style>