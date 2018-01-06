<template>
  <div id="contact-info">
    <v-container>
      <v-layout row wrap>
        <v-flex xs12>
          <h1>{{ name }}</h1>
        </v-flex>
        <v-flex xs12>
          <h2>{{ title }}</h2>
        </v-flex>
        <v-flex xs12 sm4>
          <h3>{{ location }}</h3>
        </v-flex>
        <v-flex xs12 sm4>
          <h3>{{ phone }}</h3>
        </v-flex>
        <v-flex xs12 sm4>
          <h3>{{ email }}</h3>
        </v-flex>
      </v-layout>
    </v-container>
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
      email: 'krn.x.guo@gmail.com'
    }
  }
}
</script>