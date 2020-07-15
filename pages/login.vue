<template>
  <v-app>
    <br>
    <center>
      <v-card width="420" color="#708090">
        <v-card-title>
          <h1>Login</h1>
        </v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field label="Username" prepend-icon="account_circle" /><v-text-field
              :type="showPassword ? 'text' : 'password'"
              label="Password"
              prepend-icon="mdi-lock"
              :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
              @click:append="showPassword = !showPassword"
            />
          </v-form>
        </v-card-text>
        <v-card-actions>
           <nuxt-link to="register">
             <v-btn color="warning">
            Register
          </v-btn>
           </nuxt-link>
          <v-spacer />
          <v-btn color="success">
            Login
          </v-btn>
        </v-card-actions>
      </v-card>
    </center>
    </v-card>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      showPassword: false
    }
  }
}
</script>
