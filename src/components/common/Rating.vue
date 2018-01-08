<template>
  <div>
    <v-layout row wrap>
      <v-flex xs5 class="label">
        <span class="subheading">{{ label }}</span>
      </v-flex>
      <v-flex xs7 class="rating">
        <span v-for="(i) in maxRating" :key="'filled'+i">
          <v-icon class="bubble">{{ i > rating ? 'fa-circle-o' : 'fa-circle' }}</v-icon>
        </span>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      required: true
    },
    rating: {
      type: Number,
      required: true
    }
  },
  data () {
    return {
      maxRating: 5
    }
  }
}
</script>

<style>
.bubble {
  font-size: 14px;
  margin-right: 4px;
}
.skill {
  margin-right: 6px;
  font-weight: 500;
}
@media only screen and (max-width: 600px) {
  .rating {
    text-align: right;
  }
  .label {
    text-align: left;
  }
}
</style>