<template>
  <div id="contact-info">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card>
          <v-container fill-height>
            <v-layout row wrap>
              <v-flex id="text-column" xs12 md8>
                <v-flex class="heading" xs12>
                  <h3 class="display-2">{{ name }}</h3>
                </v-flex>
                <v-flex class="heading" xs12>
                  <h5 class="headline">{{ title }}</h5>
                </v-flex>
                <v-flex class="alert-wrapper" v-if="alert" xs12>
                  <v-alert :color="alert.type" icon="priority_high" value="true">{{ alert.text }}</v-alert>
                </v-flex>
                <v-flex xs8 sm6 md12 offset-xs2 offset-sm3 offset-md0>
                  <span v-for="(ci) in contactInfo" :key="ci.method">
                    <v-layout row wrap>
                      <v-flex xs4 md6>
                        <strong>{{ ci.method }}</strong>
                      </v-flex>
                      <v-flex class="contact" xs8 md6>
                        <a v-if="ci.url" :href="ci.url">{{ ci.contact }}</a>
                        <span v-else>{{ ci.contact }}</span>
                      </v-flex>
                    </v-layout>
                  </span>
                </v-flex>
                <v-flex xs10 sm8 md12 offset-xs1 offset-sm2 offset-md0>
                  <v-layout id="social-media-icons" row wrap>
                    <v-flex md6 v-for="(sm) in socialMedia" :key="sm.icon">
                      <a v-bind:href="sm.url" target="_blank">
                        <v-icon class="social-media-icon">{{ sm.icon }}</v-icon>
                        <span class="social-media-label">{{ sm.label }}</span>
                      </a>
                    </v-flex>
                  </v-layout>
                </v-flex>
              </v-flex>
              <v-flex id="image-column" xs12 md4>
                <v-layout row-wrap align-center>
                  <v-avatar size="200">
                    <img src="../assets/profile-picture.jpg" alt="Profile Picture"/>
                  </v-avatar>
                </v-layout>
              </v-flex>
            </v-layout>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import data from '../assets/data/contact-info'

export default {
  name: 'ContactInfo',
  data () {
    return {
      name: `${data.firstName} ${data.lastName}`,
      title: data.title,
      contactInfo: data.contactInfo,
      socialMedia: data.socialMedia,
      alert: data.alert
    }
  }
}
</script>

<style scoped>
a {
  text-decoration: none;
}
.social-media-icon {
  font-size: 24px;
}
.social-media-label {
  margin-left: 6px;
  top: 6px;
  position: relative;
}
.alert-wrapper {
  padding: 0 12px;
}
@media only screen and (max-width: 960px) {
  #text-column {
    order: 2;
  }
  #image-column {
    order: 1;
  }
  #profile-picture {
    margin-top: 24px;
    margin-right: auto;
    margin-left: auto;
  }
  .contact {
    text-align: right;
  }
  #social-media-icons {
    text-align: center;
  }
}
</style>
