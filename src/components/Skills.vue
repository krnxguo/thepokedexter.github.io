<template>
  <div id="skills">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card dark color="green">
          <v-container>
            <v-flex xs12>
              <h2 class="heading headline skills-heading">Programming Langauges</h2>
              <v-layout row wrap>
                <v-flex xs12 sm6 md4 rating>
                  <rating :rating="4" label="Javascript"></rating>
                </v-flex>
                <v-flex xs12 sm6 md4 rating>
                  <rating :rating="4" label="Javascript"></rating>
                </v-flex>
                <v-flex xs12 sm6 md4 rating>
                  <rating :rating="4" label="Javascript"></rating>
                </v-flex>
                <v-flex xs12 sm6 md4 rating>
                  <rating :rating="4" label="Javascript"></rating>
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
import Rating from './common/Rating'

export default {
  components: {Rating},
  data () {
    return {}
  }
}
</script>

<style>
.skills-heading {
  margin-bottom: 24px;
}
@media only screen and (max-width: 600px) {
  .rating {
    text-align: center;
  }
}
</style>