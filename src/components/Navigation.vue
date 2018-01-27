<template>
  <div id="navigation">
    <v-layout>
      <v-toolbar class="cyan" dark dense fixed>
        <v-toolbar-items>
          <v-btn flat>Link One</v-btn>
          <v-btn flat>Link Two</v-btn>
          <v-btn flat>Link Three</v-btn>
        </v-toolbar-items>
      </v-toolbar>
    </v-layout>
  </div>
</template>
  
<script>
export default {
  data () {
    return {
      tabs: [
        {label: 'Contact Info', anchor: 'contact-info'},
        {label: 'Introduction', anchor: 'introduction'},
        {label: 'Skills', anchor: 'skills'}
      ],
      active: null
    }
  }
}
</script>

<style>
</style>