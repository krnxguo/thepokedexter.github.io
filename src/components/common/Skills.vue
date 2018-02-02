<template>
  <div id="skills">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card dark color="green">
          <v-container>
            <v-flex xs12>
              <h5 class="headline skills-heading">{{ title }}</h5>
              <v-layout row wrap>
                <v-flex v-for="(skill) in skills" :key="skill.label" xs12 sm6 md4>
                  <rating :rating="skill.rating" :label="skill.label"></rating>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import Rating from './Rating'

export default {
  name: 'Skills',
  components: { Rating },
  props: {
    title: {
      type: String,
      required: true
    },
    skills: {
      type: Array,
      required: true
    }
  },
  data () {
    return {
    }
  }
}
</script>

<style>
.skills-heading {
  margin-bottom: 24px;
}
</style>