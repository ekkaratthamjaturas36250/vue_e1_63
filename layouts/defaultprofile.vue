<template>
    <!-- App.vue -->

<v-app>
  <v-app-bar
      absolute
      color="#66CDAA">
    

     <v-card-text class="text-center"><h2>Welcome</h2></v-card-text>

      <v-spacer></v-spacer>

      

  </v-app-bar>

  <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
     color="#66CDAA"
    >
      
    </v-navigation-drawer>
  </v-card>

  <!-- Sizes your content based upon application components -->
  <v-main>

    <!-- Provides the application the proper gutter -->
    <v-container fluid>
      <!-- If using vue-router -->
      <router-view></router-view>
    </v-container>
  </v-main>

 <v-footer
    padless
  >
    <v-card
      class="flex"
      flat
      tile
    >
      <v-card-title class="teal">


        <v-spacer></v-spacer>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-6"
          dark
          icon
        >
         <v-btn icon> <v-icon size="24px">{{ icon }}</v-icon> </v-btn>
         
        </v-btn>
        <nuxt-link to="login">
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-logout</v-icon>
            </v-list-item-icon>
          </v-list-item>
           </nuxt-link>

      </v-card-title>
    </v-card>
  </v-footer>
</v-app>
</template>

<script>
  export default {
    data:function () {
    return{
       icons: [
        'mdi-account',
        'mdi-home',
        'mdi-wrench',
      ],
    }
  }
  }
</script>
