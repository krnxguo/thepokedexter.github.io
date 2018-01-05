<template>
  <div class="contact-info">
    <h1>{{ name }}</h1>
    <h2>{{ title }}</h2>
    <hr/>
    <v-container fluid grid-list>
      <v-layout>
        <v-flex d-flex xs12 sm6 md4>
          <h3>{{ location }}</h3>
        </v-flex>
        <v-flex d-flex xs12 sm6 md4>
          <h3>{{ phone }}</h3>
        </v-flex>
        <v-flex d-flex xs12 sm6 md4>
          <h3>{{ email }}</h3>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'contact-info',
  data () {
    return {
      name: 'Karen Guo',
      title: 'Full Stack Software Developer',
      location: 'Vancouver, BC',
      phone: '(778) 858-8070',
      email: 'krn.x.guo@gmail.com'
    }
  }
}
</script>

<style scoped>

</style>