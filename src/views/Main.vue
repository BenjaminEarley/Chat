<template>
<div>
  <sidebar 
    v-bind:mini="$vuetify.breakpoint.mdOnly"
    v-bind:showDrawer="$vuetify.breakpoint.mdAndUp"
    v-bind:toggle="toggle">
  </sidebar>
  <chat v-model="toggle"></chat>
</div>
</template>

<script lang="ts">
import { Component, Vue, Model } from "vue-property-decorator";
import Sidebar from "@/components/Sidebar.vue";
import Chat from "@/components/Chat.vue";

@Component({
  components: {
    Sidebar,
    Chat
  }
})
export default class Main extends Vue {
  @Model("toggle", { type: Boolean })
  toggle!: boolean;
}
</script>
