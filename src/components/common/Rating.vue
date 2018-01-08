<template>
  <div>
    <v-layout row wrap>
      <v-flex xs5>
        <span class="subheading">{{ label }}</span>
      </v-flex>
      <v-flex xs7>
        <v-icon class="bubble">fa-circle</v-icon>
        <v-icon class="bubble">fa-circle</v-icon>
        <v-icon class="bubble">fa-circle-o</v-icon>
        <v-icon class="bubble">fa-circle-o</v-icon>
        <v-icon class="bubble">fa-circle-o</v-icon>
      </v-flex>
    </v-layout>
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
.bubble {
  font-size: 14px;
}
.skill {
  margin-right: 6px;
  font-weight: 500;
}
</style>