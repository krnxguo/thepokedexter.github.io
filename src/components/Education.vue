<template>
  <div id="education">
    <section-title :title="title"/>
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card dark color="pink">
          <v-container>
            <v-layout row wrap>
              <v-flex class="graduation-cap-wrapper" xs2>
                <span class="fa-stack fa-2x">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-graduation-cap fa-stack-1x fa-inverse"></i>
                </span>
              </v-flex>
              <v-flex xs10>
                <h5 class="headline text-line">{{ education.school }}</h5>
                <h6 class="title text-line">{{ education.degree + ', ' + education.major }}</h6>
                <span class="subheading text-line">{{ 'Graduated in ' + education.graduationDate }}</span>
              </v-flex>
            </v-layout>
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
  color: #FF0056 !important;
}
.text-line {
  margin-bottom: 6px;
}
.graduation-cap-wrapper {
  align-items: center;
  display: flex;
  justify-content: center;
}
.fa-stack {
  position: absolute;
}
</style>
