<template>
  <div>
    <v-icon>fa-circle</v-icon>
    <v-icon>fa-circle</v-icon>
    <v-icon>fa-circle-o</v-icon>
    <v-icon>fa-circle-o</v-icon>
    <v-icon>fa-circle-o</v-icon>
  </div>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      required: true
    },
    rating: {
      type: Number,
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