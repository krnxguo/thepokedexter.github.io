<template>
  <div id="technologies">
    <section-title :title="title"/>
  </div>
</template>

<script>
import data from '../assets/data/skills'
import SectionTitle from './common/SectionTitle'

export default {
  components: { SectionTitle },
  data () {
    return {
      title: data.title
    }
  }
}
</script>

<style>

</style>
