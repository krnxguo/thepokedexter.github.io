<template>
  <div id="education">
    <section-title :title="title"/>
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card dark color="pink">
          <v-container>
            <v-flex xs2>
              <span class="fa-stack fa-2x">
                <i class="fa fa-circle fa-stack-2x"></i>
                <i class="fa fa-graduation-cap fa-stack-1x fa-inverse"></i>
              </span>
            </v-flex>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import data from '../assets/data/education'
import SectionTitle from './common/SectionTitle'

export default {
  components: { SectionTitle },
  data () {
    return {
      title: data.title,
      education: data.education
    }
  }

}
</script>

<style>
.fa-inverse {
  color: #FF0056;
}
</style>
