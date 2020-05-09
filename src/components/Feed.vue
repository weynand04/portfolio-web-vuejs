<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <slot />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
// Utilities
import { mapState } from "vuex";

export default {
  name: "Feed"
};
</script>
