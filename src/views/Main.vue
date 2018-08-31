<template>
<div>
  <sidebar 
    v-bind:mini="$vuetify.breakpoint.mdOnly"
    v-bind:showDrawer="$vuetify.breakpoint.mdAndUp"
    v-bind:toggle="postToggle">
  </sidebar>
  <appbar v-on:toggle="postToggle = !postToggle"></appbar>
  <chat></chat>
</div>
</template>

<script lang="ts">
import { Component, Vue, Model } from "vue-property-decorator";
import Sidebar from "@/components/Sidebar.vue";
import Appbar from "@/components/Appbar.vue";
import Chat from "@/components/Chat.vue";

@Component({
  components: {
    Sidebar,
    Appbar,
    Chat
  }
})
export default class Main extends Vue {
  postToggle: boolean = false
}
</script>
