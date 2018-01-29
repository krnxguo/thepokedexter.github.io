<template>
  <div id="navigation">
    <v-layout>
      <v-toolbar class="cyan" dark dense fixed>
        <v-toolbar-items>
          <v-btn
            v-for="tab in tabs"
            :key="tab.anchor"
            flat
            :target="'#' + tab.anchor"
          >
            {{ tab.label }}
          </v-btn>
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
        {label: 'Skills', anchor: 'skills'},
        {label: 'Tools', anchor: 'tools'}
      ],
      active: null
    }
  }
}
</script>

<style>
</style>