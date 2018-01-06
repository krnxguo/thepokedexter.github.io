<template>
  <div id="contact-info">
      <v-layout>
        <v-flex xs12 sm10 offset-sm1>
          <v-card>
            <v-container>
              <v-layout row wrap>
                <v-flex xs12>
                  <h1>{{ name }}</h1>
                </v-flex>
                <v-flex xs12>
                  <h2>{{ title }}</h2>
                </v-flex>
                <v-flex xs12>
                  <span v-for="(info) in contactInfo" :key="info.field">
                    <v-layout row wrap>
                      <v-flex xs2>
                        <strong>{{ info.field }}</strong>
                      </v-flex>
                      <v-flex xs10>
                        {{ info.value }}
                      </v-flex>
                    </v-layout>
                  </span>
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
      ]
    }
  }
}
</script>