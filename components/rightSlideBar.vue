<template>
  <v-navigation-drawer color="bg" v-model="rightSideBar" right width="260" app>
    <v-expansion-panels flat>
      <v-expansion-panel class="transparent">
        <v-expansion-panel-header>
          <v-avatar size="30">
            <img src="~/assets/image/avatar.jpg" />
          </v-avatar>
          <v-btn small text color="#7C7C7F">AAE IdeaPro</v-btn>
        </v-expansion-panel-header>
        <v-expansion-panel-content class="text-center">
          <v-btn dark small color="mainColor">profile</v-btn>
          <v-btn dark small color="mainColor">logout</v-btn>
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
    <v-divider color="grey" class="mx-6"></v-divider>
    <v-row>
      <v-col cols="6" class="px-6 py-4">
        <p class="ml-3 grey--text text-no-wrap my-2" style="font-size: 12px">
          Listeners Now
        </p>
        <p class="ml-3">1.186</p>
      </v-col>
      <v-col cols="6" class="pa-4 mt-3">
        <v-sparkline
          :value="sparkline.value"
          :smooth="sparkline.radius || false"
          :padding="sparkline.padding"
          :line-width="sparkline.width"
          :stroke-lineCap="sparkline.lineCap"
          :fill="sparkline.fill"
          :type="sparkline.type"
          :auto-line-width="sparkline.autoLineWidth"
          color="mainColor"
          :height="sparkline.height"
          auto-draw
        >
        </v-sparkline>
      </v-col>
    </v-row>

    <v-divider color="grey" class="mx-6"></v-divider>

    <v-list dense>
      <v-list-item v-for="file in flags" :key="file.title">
        <v-list-item-avatar>
          <img :src="require(`@/assets/image/${file.avatar}`)" />
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title v-text="file.title"></v-list-item-title>
        </v-list-item-content>
        <v-list-item-action>
          <v-list-item-subtitle v-text="file.subtitle"></v-list-item-subtitle>
        </v-list-item-action>
      </v-list-item>
    </v-list>
    <v-divider color="grey" class="mx-6 mb-5"></v-divider>

    <v-card dense class="mx-5 rounded-xl" style="position: relative" flat>
      <v-img height="275px" :src="require('@/assets/image/adel.jpg')">
        <div
          style="
            position: absolute;
            bottom: 0;
            margin-left: auto;
            margin-right: auto;
            right: 0px;
            text-align: center;
            left: 0;
          "
        >
          <h5 class="white--text">Miss You</h5>
          <v-slider
            v-model="sld.val"
            color="mainColor"
            track-color="white"
          ></v-slider>
          <v-card-text class="white--text d-flex justify-center align-center">
            <v-list dark dense>
              <v-list-item>
                <v-list-item-icon>
                  <v-btn icon>
                    <v-icon>mdi-rewind</v-icon>
                  </v-btn>
                </v-list-item-icon>
                <v-list-item-icon>
                  <v-btn @click="sld.pause = !sld.pause" icon>
                    <v-icon>
                      {{
                        sld.pause ? "mdi-pause" : "mdi-skip-next-circle-outline"
                      }}
                    </v-icon>
                  </v-btn>
                </v-list-item-icon>
                <v-list-item-icon>
                  <v-btn icon>
                    <v-icon>mdi-fast-forward</v-icon>
                  </v-btn>
                </v-list-item-icon>
              </v-list-item>
            </v-list>
          </v-card-text>
        </div>
      </v-img>
    </v-card>
  </v-navigation-drawer>
</template>

<script>
export default {
  data() {
    return {
      rightSideBar: true,
      sparkline: {
        width: 5,
        radius: 10,
        padding: 8,
        lineCap: "round",
        value: [0, 2, 5, 9, 5, 10, 3, 5],
        fill: false,
        type: "trend",
        autoLineWidth: false,
        height: 150,
      },
      flags: [
        {
          avatar: "us.png",
          title: "United States",
          subtitle: "64%",
        },
        {
          avatar: "uk.png",
          title: "United Kingdom",
          subtitle: "12%",
        },
        {
          avatar: "ca.png",
          title: "Canada",
          subtitle: "9%",
        },
        {
          avatar: "au.png",
          title: "Australia",
          subtitle: "4%",
        },
      ],
      sld: {
        val: 25,
        pause: true,
      },
    };
  },
};
</script>

