<template>
  <div id = "app">
    <input v-model="a">+
    <input v-model="b">=
    {{c}}
    <button v-on:click="sum">Sum</button>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  el: "#app",
  data: ()=>({
    a:"11",
    b:"22",
    c:0
  }),
  methods: {
    sum: function() {
      this.c = parseInt(this.a) +parseInt(this.b);
    }
  }
});
</script>
