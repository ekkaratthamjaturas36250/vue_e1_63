<template>
   <v-app>

        <v-system-bar
          color="#4169E1"
          :height="height"
          :lights-out="lightsOut"
          :window="window"
        >
          <v-spacer></v-spacer>
          <v-icon>mdi-wifi-strength-4</v-icon>
          <v-icon>mdi-signal-cellular-outline</v-icon>
          <v-icon>mdi-battery</v-icon>
          <span>12:30</span>
        </v-system-bar>

    <v-card color="#1E90FF">
        <v-row>
        <v-col cols="10">
      <v-icon color="#ffffff" class="mr-4 mb-2 ml-7">mdi-view-list</v-icon>
      <strong class="fontcolor" style="font-size: 24px;">Destination</strong>
</v-col>
        <v-icon color="#ffffff">mdi-magnify</v-icon>
    </v-row>

    </v-card>

    <v-content>

        <nuxt></nuxt>
    </v-content>

   </v-app>

</template>

<style>
.fontcolor {
    color:#ffffff;
}
</style>
