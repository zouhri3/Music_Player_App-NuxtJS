<template>
  <v-navigation-drawer
    app
    fixed
    clipped
    mini-variant
    mini-variant-width="100"
    v-model="sideBar"
    permanent
    color="bg"
    class="sideBar"
  >
    <div style="border-bottom: 0.5px solid rgba(255, 255, 255, 0.12)">
      <v-avatar size="100" class="d-block text-center">
        <v-icon color="mainColor" size="60">mdi-movie-roll mdi-spin</v-icon>
      </v-avatar>
    </div>
    <v-list flat>
      <v-list-item
        v-for="(item, i) in items"
        :key="i"
        :ripple="false"
        nuxt
        :to="item.router"
        active-class="activeList"
        v-slot="{ active }"
      >
        <v-list-item-icon>
          <v-icon
            :color="active ? 'mainColor' : 'grey'"
            size="32"
            :style="{ textShadow: active ? '0 0 25px' : '' }"
            >{{ item.icon }}</v-icon
          >
        </v-list-item-icon>
      </v-list-item>
    </v-list>
    <v-list>
      <v-list-item>
        <v-icon
          size="30"
          @click="modeSwitcher()"
          style="text-shadow: 0 0 25px; cursor: pointer"
          color="mainColor"
          >{{
            $vuetify.theme.dark ? "mdi-weather-night" : "mdi-weather-sunny"
          }}</v-icon
        >
      </v-list-item>
      <v-list-item>
        <v-icon>mdi-help-circle-outline</v-icon>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  data() {
    return {
      sideBar: true,
      selectedItem: 1,
      items: [
        {
          icon: "mdi-radio-tower",
          router: "/",
        },
        {
          icon: "mdi-music",
          router: "/player",
        },
      ],
    };
  },

  methods: {
    modeSwitcher() {
      this.$vuetify.theme.dark = !this.$vuetify.theme.dark;
    },
  },
};
</script>

<style   lang="scss" >
.sideBar .v-navigation-drawer__content {
  height: 100%;
  overflow-y: auto;
  overflow-x: hidden;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>>

