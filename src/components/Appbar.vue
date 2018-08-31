<template>
  <v-toolbar fixed app>
    <v-toolbar-side-icon 
      class="hidden-md-and-up" 
      v-on:click="$emit('toggle')">
    </v-toolbar-side-icon>
    <v-toolbar-title></v-toolbar-title>
  </v-toolbar>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Appbar extends Vue {}
</script>

