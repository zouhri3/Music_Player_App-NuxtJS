<template>
  <v-app>
    <side-bar />
    <v-divider />
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import sideBar from "../components/sideBar.vue";
export default {
  components: { sideBar },
  name: "DefaultLayout",
  data() {
    return {
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/",
        },
      ],
    };
  },
};
</script>
