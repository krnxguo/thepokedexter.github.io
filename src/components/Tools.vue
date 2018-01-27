<template>
  <div id="skills">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card dark color="purple">
          <v-container>
            <v-flex xs12>
              <h2 class="headline tools-heading">{{ title }}</h2>
              <v-layout row wrap>
                <v-flex v-for="(tool) in tools" :key="tool.label" xs12 sm6 md4>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import data from '../assets/data/tools'

export default {
  name: 'Tools',
  data () {
    return {
      title: data.title,
      tools: data.tools
    }
  }
}
</script>

<style>
.tools-heading {
  margin-bottom: 24px;
}
</style>