<template>
  <div>
    <span class="subheading skill">{{ label }}</span>
    <v-icon class="bubble">fa-circle</v-icon>
    <v-icon class="bubble">fa-circle</v-icon>
    <v-icon class="bubble">fa-circle-o</v-icon>
    <v-icon class="bubble">fa-circle-o</v-icon>
    <v-icon class="bubble">fa-circle-o</v-icon>
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
  font-size: 16px;
}
.skill {
  margin-right: 6px;
  font-weight: 500;
}
</style>