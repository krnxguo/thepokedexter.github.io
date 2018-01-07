<template>
  <div id="skills">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card dark color="green">
          <v-container>
            <v-flex xs12>
              <h2 class="heading">Skills</h2>
              <rating></rating>
            </v-flex>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import Rating from './common/Rating'

export default {
  components: {Rating},
  data () {
    return {}
  }
}
</script>

<style>
</style>