<template>
    <!-- App.vue -->

<v-app>
  <v-app-bar app :collapse="!collapseOnScroll"
      :collapse-on-scroll="collapseOnScroll"
      absolute
      scroll-target="#scrolling-techniques-6">
    
    <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

      <v-toolbar-title>Chaiyaphum Technical College</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-checkbox
        v-model="collapseOnScroll"
        color="white"
        hide-details
      ></v-checkbox>

  </v-app-bar>

  <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list
        nav
        dense
      >
          <nuxt-link to="/">
          <v-list-item>
            <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>
          </nuxt-link>

         <nuxt-link to="login">
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Login</v-list-item-title>
          </v-list-item>
           </nuxt-link>

        </v-list-item-group>
      </v-list>
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

  <v-footer app>
    <!-- -->
  </v-footer>
</v-app>
</template>

<script>
  export default {
    data: () => ({
      drawer: false,
      collapseOnScroll: true,
    }),
  }
</script>