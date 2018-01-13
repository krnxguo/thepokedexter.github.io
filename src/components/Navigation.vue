<template>
  <div id="navigation">
    <v-layout>
      <v-tabs id="tabs" class="elevation-3">
        <v-tabs-bar class="cyan" dark>
          <v-tabs-item>
            Tab1
          </v-tabs-item>
          <v-tabs-item>
            Tab2
          </v-tabs-item>
        </v-tabs-bar>
      </v-tabs>
    </v-layout>
  </div>
</template>
  
<script>
export default {
  data () {
    return {}
  }
}
</script>

<style>
#tabs {
  position: fixed;
  z-index: 3;
}
</style>