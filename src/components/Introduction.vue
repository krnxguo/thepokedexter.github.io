<template>
  <div id="introduction">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card>
          <v-container>
            <v-flex xs12>
              <h5 class="headline">{{ title }}</h5>
            </v-flex>
            <v-flex xs12>
              <p v-for="(paragraph, index) in blurb" :key="index">
                {{ paragraph }}
              </p>
            </v-flex>
            <hr/>
            <v-layout row justify-center>
              <v-card-actions id="action-button-row">
                <v-btn v-on:click="viewResume(resumeUrl)" large color="primary">View PDF Resume</v-btn>
              </v-card-actions>
            </v-layout>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import data from '../assets/data/introduction'

export default {
  data () {
    return {
      blurb: data.blurb,
      title: data.title,
      resumeUrl: data.resumeUrl
    }
  },
  methods: {
    viewResume: function (url) {
      window.open(url, '_blank')
    }
  }
}
</script>

<style>
#action-button-row {
  margin-top: 16px;
  margin-bottom: 16px;
}
</style>