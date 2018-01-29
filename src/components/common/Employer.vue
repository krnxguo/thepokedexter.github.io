<template>
  <div id="employer">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card>
          <v-toolbar class="blue" dark flat>
            <v-toolbar-title>MS/MRI Lab</v-toolbar-title>
          </v-toolbar>
          <v-container>
            MY WORK MY WORK MY WORK
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
    }
  },
  data() {
    return {}
  }
}
</script>

<style>
</style>