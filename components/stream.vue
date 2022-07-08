<template>
  <v-card class="rounded-lg" color="bg">
    <v-toolbar color="transparent" flat class="py-4">
      <v-toolbar-title class="mt-n5">
        <span class="caption d-block">Streams</span>450,210
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <div class="text-center">
        <v-avatar size="40px">
          <img :src="require('@/assets/image/all.png')" />
        </v-avatar>
        <span class="caption d-block">ALL</span>
      </div>

      <div class="text-center ml-14">
        <v-avatar size="40px">
          <img :src="require('@/assets/image/spotify.png')" />
        </v-avatar>
        <span class="caption d-block">Spotify</span>
      </div>
      <div class="text-center ml-14">
        <v-avatar size="40px">
          <img :src="require('@/assets/image/youtube.png')" />
        </v-avatar>
        <span class="caption d-block">YouTube</span>
      </div>
      <div class="text-center ml-14">
        <v-avatar size="40px">
          <img :src="require('@/assets/image/music.png')" />
        </v-avatar>
        <span class="caption d-block">Apple Music</span>
      </div>
      <div class="text-center ml-12">
        <v-btn small icon class="d-block">
          <v-icon color="mainColor"> mdi-arrow-right </v-icon>
        </v-btn>
        <v-btn small icon class="d-block mt-2">
          <v-icon color="grey"> mdi-arrow-left </v-icon>
        </v-btn>
      </div>
    </v-toolbar>
    <div class="mt-5">
      <line-chart
        :chart-id="chartId"
        :width="width"
        :height="height"
        :css-classes="cssClasses"
        :styles="styles"
        :plugins="plugins"
      />
    </div>
  </v-card>
</template>
<script>
import LineChart from "@/chart_js/line.js";
export default {
  components: { LineChart },
  props: {
    chartId: {
      type: String,
      default: "line-chart",
    },
    width: {
      type: Number,
      default: 400,
    },
    height: {
      type: Number,
      default: 230,
    },
    cssClasses: {
      default: "",
      type: String,
    },
    styles: {
      type: Object,
      default: () => {},
    },
    plugins: {
      type: Array,
      default: () => {},
    },
  },
};
</script>
