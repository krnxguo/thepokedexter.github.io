<template>
  <div id="navigation">
    <v-layout>
      <v-tabs id="tabs" class="elevation-3" v-model="active">
        <v-tabs-bar class="cyan" dark>
          <v-tabs-item
            v-for="tab in tabs"
            :key="tab"
            :href="'#' + tab"
            ripple
          >
            {{ tab }}
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
        'Contact Info',
        'Introduction',
        'Skills'
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