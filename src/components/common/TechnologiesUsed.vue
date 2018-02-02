<template>
  <span v-if="technologies.length > 0">
    <hr/>
    <h6 class="technologies-used-title">{{ title }}</h6>
    <div class="technologies">
      <v-chip v-for="(technology) in technologies" :key="technology">
        <strong>{{ technology }}</strong>
      </v-chip>
    </div>
  </span>
</template>

<script>
export default {
  props: {
    technologies: {
      type: Array,
      default: function () {
        return []
      }
    },
    title: {
      type: String,
      default: function () {
        return 'Technologies Used'
      }
    }
  },
  data () {
    return {}
  }
}
</script>

<style>
.technologies-used-title {
  margin: 16px 0 12px 5px;
  font-size: 15px;
  font-weight: 500;
  text-transform: uppercase;
}
.technologies {
  margin-bottom: 8px;
}
</style>
