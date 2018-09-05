<template>
  <v-form>
    <v-text-field 
      hide-details 
      solo
      clearable
      placeholder="Say Something..."
      type="text"
      append-outer-icon="send">
    </v-text-field>
  </v-form>
</template>



<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class MessageField extends Vue {}
</script>