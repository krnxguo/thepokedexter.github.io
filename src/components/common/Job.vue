<template>
  <v-card>
    <v-toolbar class="blue" dark flat extended>
      <v-toolbar-title>{{ employer }}</v-toolbar-title>
      <v-toolbar-title slot="extension">{{ position }}</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-title>{{ startDate + " - " + endDate}}</v-toolbar-title>
    </v-toolbar>
    <v-container>
      MY WORK MY WORK MY WORK
    </v-container>
  </v-card>
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
</style>