<template>
<div>
  <sidebar 
    v-bind:mini="$vuetify.breakpoint.mdOnly"
    v-bind:showDrawer="$vuetify.breakpoint.mdAndUp">
  </sidebar>
  <chat></chat>
</div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Sidebar from "@/components/Sidebar.vue";
import Chat from "@/components/Chat.vue";

@Component({
  components: {
    Sidebar,
    Chat
  }
})
export default class Main extends Vue {}
</script>
