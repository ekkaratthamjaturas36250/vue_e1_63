<template>
  <v-app>
    <v-card>
      <v-card-title>
        <h1>Login</h1>
      </v-card-title>
      <v-card-text>
        <v-form>
          <v-text-field label="Username" prepend-icon="account_circle" />
          <v-text-field type="password" label="Password" prepend-icon="mdi-lock" append-icon="visibility_off" />
        </v-form>
      </v-card-text>
      <v-card-actions>
        <v-btn color="warning">Register</v-btn>
        <v-spacer></v-spacer>
        <v-btn color="success">Login</v-btn>
      </v-card-actions>
      </v-card>
  </v-app>
</template>
