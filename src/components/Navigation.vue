<template>
  <div id="navigation">
    <v-layout>
      <v-tabs v-model="active">
        <v-tabs-bar class="cyan">
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
