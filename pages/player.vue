<template>
  <v-container>
    <v-row>
      <v-col>
        <v-card dense class="mx-5 rounded-xl" style="position: relative" flat>
          <v-img height="91vh" :src="require('@/assets/image/adel.jpg')">
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
              <v-card-text
                class="white--text d-flex justify-center align-center"
              >
                <v-list color="transparent" dense>
                  <v-list-item>
                    <v-list-item-icon>
                      <v-btn color="white" icon>
                        <v-icon>mdi-rewind</v-icon>
                      </v-btn>
                    </v-list-item-icon>
                    <v-list-item-icon>
                      <v-btn color="white" @click="sld.pause = !sld.pause" icon>
                        <v-icon>
                          {{
                            sld.pause
                              ? "mdi-pause"
                              : "mdi-skip-next-circle-outline"
                          }}
                        </v-icon>
                      </v-btn>
                    </v-list-item-icon>
                    <v-list-item-icon>
                      <v-btn color="white" icon>
                        <v-icon>mdi-fast-forward</v-icon>
                      </v-btn>
                    </v-list-item-icon>
                  </v-list-item>
                </v-list>
              </v-card-text>
            </div>
          </v-img>
        </v-card>
      </v-col>
      <v-col>
        <v-card color="bg">
          <v-toolbar color="transparent" flat class="py-4">
            <v-toolbar-title class="mt-n10">
              <span class="h2 text-uppercase white--text">list music</span>
            </v-toolbar-title>
          </v-toolbar>

          <v-divider color="grey" class="mx-6 mt-3 mb-2"></v-divider>
          <v-list subheader flat color="transparent">
            <v-list-item class="py-n8">
              <span class="mr-2 caption">01</span>
              <v-list-item-avatar class="mr-2" rounded>
                <v-img :src="require('@/assets/image/1.jpg')" />
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>Who Cares</v-list-item-title>
                <v-list-item-subtitle class="caption"
                  >93k plays</v-list-item-subtitle
                >
              </v-list-item-content>
              <v-list-item-action>
                <v-btn icon>
                  <v-icon color="grey lighten-1" small
                    >mdi-chevron-right</v-icon
                  >
                </v-btn>
              </v-list-item-action>
            </v-list-item>

            <v-divider color="grey" class="mx-6"></v-divider>
            <v-list-item>
              <span class="mr-2 caption">02</span>
              <v-list-item-avatar class="mr-2" rounded>
                <v-img :src="require('@/assets/image/2.jpg')" />
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>Miss You</v-list-item-title>
                <v-list-item-subtitle class="caption"
                  >64k plays</v-list-item-subtitle
                >
              </v-list-item-content>
              <v-list-item-action>
                <v-btn icon>
                  <v-icon color="grey lighten-1" small
                    >mdi-chevron-right</v-icon
                  >
                </v-btn>
              </v-list-item-action>
            </v-list-item>

            <v-divider color="grey" class="mx-6"></v-divider>
            <v-list-item>
              <span class="mr-2 caption">03</span>
              <v-list-item-avatar class="mr-2" rounded>
                <v-img :src="require('@/assets/image/3.jpg')" />
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>WorldWide</v-list-item-title>
                <v-list-item-subtitle class="caption"
                  >59k plays</v-list-item-subtitle
                >
              </v-list-item-content>
              <v-list-item-action>
                <v-btn icon>
                  <v-icon color="grey lighten-1" small
                    >mdi-chevron-right</v-icon
                  >
                </v-btn>
              </v-list-item-action>
            </v-list-item>
            <v-divider color="grey" class="mx-6"></v-divider>

            <v-list-item>
              <span class="mr-2 caption">03</span>
              <v-list-item-avatar class="mr-2" rounded>
                <v-img :src="require('@/assets/image/3.jpg')" />
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>WorldWide</v-list-item-title>
                <v-list-item-subtitle class="caption"
                  >59k plays</v-list-item-subtitle
                >
              </v-list-item-content>
              <v-list-item-action>
                <v-btn icon>
                  <v-icon color="grey lighten-1" small
                    >mdi-chevron-right</v-icon
                  >
                </v-btn>
              </v-list-item-action>
            </v-list-item>
            <v-divider color="grey" class="mx-6"></v-divider>

            <v-list-item class="py-n8">
              <span class="mr-2 caption">04</span>
              <v-list-item-avatar class="mr-2" rounded>
                <v-img :src="require('@/assets/image/4.jpg')" />
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>Like Me</v-list-item-title>
                <v-list-item-subtitle class="caption"
                  >21k plays</v-list-item-subtitle
                >
              </v-list-item-content>
              <v-list-item-action>
                <v-btn icon>
                  <v-icon color="grey lighten-1" small
                    >mdi-chevron-right</v-icon
                  >
                </v-btn>
              </v-list-item-action>
            </v-list-item>
            <v-divider color="grey" class="mx-6"></v-divider>
            <v-list-item>
              <span class="mr-2 caption">05</span>
              <v-list-item-avatar class="mr-2" rounded>
                <v-img :src="require('@/assets/image/5.jpg')" />
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>No Surprise</v-list-item-title>
                <v-list-item-subtitle class="caption"
                  >23k plays</v-list-item-subtitle
                >
              </v-list-item-content>
              <v-list-item-action>
                <v-btn icon>
                  <v-icon color="grey lighten-1" small
                    >mdi-chevron-right</v-icon
                  >
                </v-btn>
              </v-list-item-action>
            </v-list-item>
            <v-divider color="grey" class="mx-6"></v-divider>
            <v-list-item>
              <span class="mr-2 caption">06</span>
              <v-list-item-avatar class="mr-2" rounded>
                <v-img :src="require('@/assets/image/7.jpg')" />
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>Each Time</v-list-item-title>
                <v-list-item-subtitle class="caption"
                  >12k plays</v-list-item-subtitle
                >
              </v-list-item-content>
              <v-list-item-action>
                <v-btn icon>
                  <v-icon color="grey lighten-1" small
                    >mdi-chevron-right</v-icon
                  >
                </v-btn>
              </v-list-item-action>
            </v-list-item>

            <v-divider color="grey" class="mx-6"></v-divider>

            <v-divider color="grey" class="mx-6"></v-divider>
            <v-list-item class="py-n8">
              <span class="mr-2 caption">01</span>
              <v-list-item-avatar class="mr-2" rounded>
                <v-img :src="require('@/assets/image/1.jpg')" />
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>Who Cares</v-list-item-title>
                <v-list-item-subtitle class="caption"
                  >93k plays</v-list-item-subtitle
                >
              </v-list-item-content>
              <v-list-item-action>
                <v-btn icon>
                  <v-icon color="grey lighten-1" small
                    >mdi-chevron-right</v-icon
                  >
                </v-btn>
              </v-list-item-action>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "player",
  data() {
    return {
      sld: {
        val: 25,
        pause: true,
      },
    };
  },
};
</script>