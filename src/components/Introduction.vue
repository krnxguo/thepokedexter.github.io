<template>
  <div id="introduction">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card>
          <v-container>
            <v-flex xs12>
              <h2 class="headline">{{ title }}</h2>
            </v-flex>
            <v-flex xs12>
              <p>
                {{ blurb }}
              </p>
            </v-flex>
            <hr/>
            <v-layout row justify-center>
              <v-card-actions id="action-button-row">
                <!-- TODO: Add link to Google Docs resume -->
                <v-btn large color="primary">View Resume</v-btn>
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
      title: data.title
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