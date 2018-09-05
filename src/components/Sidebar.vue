<template>
    <v-navigation-drawer 
      v-model="drawer"
      :mini-variant="mini"
      app
      :permanent="showDrawer">
      <v-toolbar flat>
        <v-list>
          <v-list-tile>
            <v-list-tile-title class="title">
              Chat
            </v-list-tile-title>
          </v-list-tile>
        </v-list>
      </v-toolbar>
      <v-divider></v-divider>
      <v-list class="pt-0">
        <v-list-tile
          v-for="item in items"
          :key="item.id"
        >
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>
  
          <v-list-tile-content>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
</template>

<script lang="ts">
import { Component, Prop, Vue, Watch } from "vue-property-decorator";

@Component
export default class Sidebar extends Vue {
  drawer: any = null;
  items = [
    { id: 0, title: "All",    icon: "question_answer" },
    { id: 1, title: "Chat 1", icon: "question_answer" },
    { id: 2, title: "Chat 2", icon: "question_answer" },
    { id: 3, title: "Chat 3", icon: "question_answer" },
    { id: 4, title: "Chat 4", icon: "question_answer" },
    { id: 5, title: "Chat 5", icon: "question_answer" }
  ];
  @Prop(Boolean) mini!: boolean;
  @Prop(Boolean) showDrawer!: boolean;
  @Prop(Boolean) toggle!: boolean;

  @Watch("toggle")
  onChildChanged(val: boolean, oldVal: boolean) {
    console.log(oldVal + " to " + val);
    this.drawer = !this.drawer;
  }
}
</script>

