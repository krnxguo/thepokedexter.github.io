<template>
  <div id="technologies">
    <section-title :title="title"/>
    <skills
      v-for="skill in skills" :key="skill.skillType"
      :title="skill.skillType"
      :skills="skill.skills"
    />
  </div>
</template>

<script>
import skillsData from '../assets/data/skills'

import Skills from './common/Skills'
import SectionTitle from './common/SectionTitle'

export default {
  components: { Skills, SectionTitle },
  data () {
    return {
      title: skillsData.title,
      skills: skillsData.skills
    }
  }
}
</script>

<style>

</style>
