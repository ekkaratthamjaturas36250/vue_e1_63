<template>
  <v-container fluid class="pa-0">
    <v-row align="center">
      <v-col cols="12" sm="6">
        <div class="text-center">
          <div class="my-2">
            <nuxt-link to="activity/acti_flag">
              <v-btn color="#AED581" dark>
                กิจกรรมเข้าแถว
              </v-btn>
            </nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="activity/acti_homeroom">
              <v-btn color="#4DD0E1" dark>
                กิจกรรมโฮมรูม
              </v-btn>
            </nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="activity/acti_profes">
              <v-btn color="warning" dark>
                กิจกรรมชมรม
              </v-btn>
            </nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="activity/acti_spe">
              <v-btn color="#B39DDB" dark large>
                กิจกรรมพิเศษ
              </v-btn>
            </nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="/#/">
              <v-btn x-large color="error" dark>
                กลับหน้าหลัก
              </v-btn>
            </nuxt-link>
          </div>
        </div>
      </v-col>
      <v-col cols="12" sm="6">
        <div class="text-center">
          <div class="my-2">
            <v-btn color="secondary" fab x-small dark>
              <v-icon>mdi-television</v-icon>
            </v-btn>
          </div>
          <div class="my-2">
            <v-btn color="primary" fab small dark>
              <v-icon>mdi-pencil</v-icon>
            </v-btn>
          </div>
          <div class="my-2">
            <v-btn color="warning" fab dark>
              <v-icon>mdi-account-circle</v-icon>
            </v-btn>
          </div>
          <div class="my-2">
            <v-btn color="error" fab large dark>
              <v-icon>mdi-alarm</v-icon>
            </v-btn>
          </div>
          <div class="my-2">
            <v-btn color="success" fab x-large dark>
              <v-icon>mdi-domain</v-icon>
            </v-btn>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>
