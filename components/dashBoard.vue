<template>
  <v-container>
    <v-toolbar color="transparent" flat>
      <v-toolbar-title class="mt-n3">Overview</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text class="withoutupercase">
        Last 30 Days
        <v-icon color="mainColor" class="d-inline-block mx-6">
          mdi-chevron-down</v-icon
        >
      </v-btn>
    </v-toolbar>
    <v-row>
      <v-col cols="12" sm="8"> <stream /> </v-col>
      <v-col cols="12" sm="4"> <earning /> </v-col>
      <v-col cols="12" sm="4">
        <audience />
      </v-col>
      <v-col cols="12" sm="8">
        <release />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Audience from "./audience.vue";
import Earning from "./earning.vue";
import Release from "./release.vue";
import stream from "./stream.vue";
export default {
  components: { stream, Earning, Audience, Release },
};
</script>