<template>
  <div id="contact-info">
      <v-layout>
        <v-flex xs12 sm10 lg8 offset-sm1 offset-lg2>
          <v-card>
            <v-container fill-height>
              <v-layout row wrap>
                <v-flex xs12 md8>
                  <v-flex xs12>
                    <h1>{{ name }}</h1>
                  </v-flex>
                  <v-flex xs12>
                    <h2>{{ title }}</h2>
                  </v-flex>
                  <v-flex xs12>
                    <span v-for="(info) in contactInfo" :key="info.field">
                      <v-layout row wrap>
                        <v-flex xs2 md4>
                          <strong>{{ info.field }}</strong>
                        </v-flex>
                        <v-flex xs10 md8>
                          {{ info.value }}
                        </v-flex>
                      </v-layout>
                    </span>
                  </v-flex>
                  <v-flex xs12 md12>
                    <v-layout row wrap>
                      <v-flex xs6 sm4 v-for="(icon) in iconLinks" :key="icon.icon">
                        <a v-bind:href="icon.link" target="_blank">
                          <v-icon>{{ icon.icon }}</v-icon>
                          {{ icon.label }}
                        </a>
                      </v-flex>
                    </v-layout>
                  </v-flex>
                </v-flex>
                <v-flex xs12 md4>
                  <v-layout row-wrap align-center>
                    <img id="profile-picture" src="/static/default-profile-pic.jpg" alt="Profile Picture"/>
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
        {field: 'Location', value: 'Vancouver, BC'},
        {field: 'Phone', value: '778.858.8070'},
        {field: 'Email', value: 'krn.x.guo@gmail.com'}
      ],
      iconLinks: [
        {icon: 'fa-github', link: 'https://github.com/ThePokedexter', label: 'ThePokedexter'},
        {icon: 'fa-linkedin-square', link: 'https://linkedin.com/in/kxguo', label: 'kxguo'}
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
</style>
