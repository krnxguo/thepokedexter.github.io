<template>
  <div id="introduction">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card>
          <v-container>
            <p>
              Full stack developer with professional experience in modern web frameworks. 
              Lifelong learner who values clean code, best practises, and effective team communication.
            </p>
            <hr/>
            <v-layout row justify-center>
              <v-card-actions id="action-button-row">
                <v-btn large color="success">Download Resume</v-btn>
              </v-card-actions>
            </v-layout>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {
  data () {
    return {}
  }
}
</script>

<style>
p {
  margin: 8px 8px 24px 8px;
}
#action-button-row {
  margin-top: 16px;
  margin-bottom: 16px;
}
</style>