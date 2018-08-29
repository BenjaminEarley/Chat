<template>
  <div>
    <v-toolbar fixed app>
      <v-toolbar-side-icon class="hidden-md-and-up" v-on:click="toggleSidebar"></v-toolbar-side-icon>
      <v-toolbar-title></v-toolbar-title>
    </v-toolbar>
    <v-content>
      <v-container fluid fill-height>

      </v-container>
    </v-content>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop, Emit } from "vue-property-decorator";

@Component
export default class Chat extends Vue {
  @Prop(Boolean) toggle!: boolean;

  @Emit("toggle")
  toggleSidebar() {
    this.toggle = !this.toggle;
  }
}
</script>

