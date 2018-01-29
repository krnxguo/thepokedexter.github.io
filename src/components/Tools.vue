<template>
  <div id="skills">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card dark color="purple">
          <v-container>
            <v-flex xs12>
              <h5 class="headline tools-heading">{{ title }}</h5>
              <v-layout v-for="(toolSection) in tools" :key="toolSection.toolType" row wrap>
                <v-flex xs4>
                  <span class="subheading">{{ toolSection.toolType }}</span>
                </v-flex>
                <v-flex class="tools" xs8>
                  <span class="subheading" v-for="(tool, index) in toolSection.tools" :key="tool.label">
                    {{ index === toolSection.tools.length - 1 ? tool.label : tool.label + ','}}
                  </span>
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
@media only screen and (min-width: 600px) {
  .tools {
    text-align: right;
  }
}
</style>