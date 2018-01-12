<template>
  <div id="contact-info">
    <v-layout>
      <v-flex xs12 sm10 lg8 offset-xs0 offset-sm1 offset-lg2>
        <v-card>
          <v-container fill-height>
            <v-layout row wrap>
              <v-flex id="text-column" xs12 md8>
                <v-flex class="heading" xs12>
                  <h1 class="display-2">{{ name }}</h1>
                </v-flex>
                <v-flex class="heading" xs12>
                  <h2 class="headline">{{ title }}</h2>
                </v-flex>
                <v-flex xs8 sm6 md12 offset-xs2 offset-sm3 offset-md0>
                  <span v-for="(ci) in contactInfo" :key="ci.method">
                    <v-layout row wrap>
                      <v-flex xs4 md6>
                        <strong>{{ ci.method }}</strong>
                      </v-flex>
                      <v-flex class="contact" xs8 md6>
                        {{ ci.contact }}
                      </v-flex>
                    </v-layout>
                  </span>
                </v-flex>
                <v-flex xs10 sm8 md12 offset-xs1 offset-sm2 offset-md0>
                  <v-layout id="social-media-icons" row wrap>
                    <v-flex v-for="(sm) in socialMedia" :key="sm.icon">
                      <a v-bind:href="sm.url" target="_blank">
                        <v-icon class="social-media-icon">{{ sm.icon }}</v-icon>
                        {{ sm.label }}
                      </a>
                    </v-flex>
                  </v-layout>
                </v-flex>
              </v-flex>
              <v-flex id="image-column" xs12 md4>
                <v-layout row-wrap align-center>
                  <img id="profile-picture" src="../assets/default-profile-pic.jpg" alt="Profile Picture"/>
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
export default {
  name: 'ContactInfo',
  data () {
    return {
      name: 'Karen Guo',
      title: 'Full Stack Software Developer',
      location: 'Vancouver, BC',
      phone: '778.858.8070',
      email: 'krn.x.guo@gmail.com',
      contactInfo: [
        {method: 'Location', contact: 'Vancouver, BC'},
        {method: 'Phone', contact: '778.858.8070'},
        {method: 'Email', contact: 'krn.x.guo@gmail.com'}
      ],
      socialMedia: [
        {icon: 'fa-github', url: 'https://github.com/ThePokedexter', label: 'ThePokedexter'},
        {icon: 'fa-linkedin-square', url: 'https://linkedin.com/in/kxguo', label: 'kxguo'}
      ]
    }
  }
}
</script>

<style scoped>
a {
  text-decoration: none;
}
#profile-picture {
  border-radius: 50%;
  width: 200px;
  height: 200px;
}
.social-media-icon {
  font-size: 24px;
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
