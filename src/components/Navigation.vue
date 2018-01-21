<template>
  <div id="navigation">
    <v-layout>
      <v-tabs id="tabs" class="elevation-3" v-model="active">
        <v-tabs-bar class="cyan" dark>
          <v-tabs-item
            v-for="tab in tabs"
            :key="tab.anchor"
            :href="'#' + tab.anchor"
            ripple
          >
            {{ tab.label }}
          </v-tabs-item>
          <v-tabs-slider color="yellow"></v-tabs-slider>
        </v-tabs-bar>
      </v-tabs>
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
#tabs {
  position: fixed;
  z-index: 3;
}
</style>