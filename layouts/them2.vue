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
      <v-icon color="#ffffff" class="mr-4 mb-1 ml-7">mdi-arrow-left</v-icon>
      <strong class="fontcolor" style="font-size: 24px;">Welcome</strong>
</v-col>
        <v-icon color="#ffffff">mdi-magnify</v-icon>
        <v-icon color="#ffffff">mdi-dots-vertical</v-icon>
    </v-row>
    <br>


    <v-row class="text-center">
     
        <v-tabs background-color="#1E90FF" color="#ffffff">
        <v-col cols="6">
            <v-tab>SIGN UP</v-tab>
        </v-col>

        <v-col cols="6">
                <v-tab>SIGN IN</v-tab>
        </v-col>
         </v-tabs>

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
