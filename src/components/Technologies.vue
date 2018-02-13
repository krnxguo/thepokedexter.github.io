<template>
  <div id="technologies">
    <section-title :title="title"/>
    <skills
      v-for="skill in skills" :key="skill.skillType"
      :title="skill.skillType"
      :skills="skill.skills"
    />
    <tools
      v-for="tool in tools" :key="tool.title"
      :title="tool.title"
      :tools="tool.tools"
    />
  </div>
</template>

<script>
import data from '../assets/data/technologies'

import Skills from './subsections/Skills'
import SectionTitle from './common/SectionTitle'
import Tools from './subsections/Tools'

export default {
  components: { Skills, SectionTitle, Tools },
  data () {
    return {
      title: data.title,
      skills: data.skills,
      tools: data.tools
    }
  }
}
</script>

<style>

</style>
