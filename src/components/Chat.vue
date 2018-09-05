<template>
  <v-content>
    <v-container fluid>
      <v-layout row fill-height>
        <v-flex xs12>
          <div></div>
        </v-flex>
      </v-layout>
      <v-layout absolute bottom row justify-center>
        <v-flex xs12 lg10>
          <message-field></message-field>
        </v-flex>
      </v-layout>
    </v-container>
  </v-content>  
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import MessageField from "@/components/MessageField.vue";

@Component({
  components: {
    MessageField
  }
})
export default class Chat extends Vue {}
</script>

