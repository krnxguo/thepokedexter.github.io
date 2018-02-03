<template>
  <v-layout>
    <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
      <h3 class="display-1 section-title">{{ title }}</h3>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  props: {
    title: {
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
.section-title {
  text-align: center;
  color: #494949;
  margin-top: 2.25rem;
  margin-bottom: 1rem;
  font-weight: 500;
}
</style>
