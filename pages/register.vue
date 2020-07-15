<template>
  <v-app>
    <br>
    <center>
      <v-card width="650" color="#708090">
        <v-card-title>
          <h1>Register</h1>
        </v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field label="Name & Lastname" prepend-icon="accessibility" />
            <v-text-field label="Username" prepend-icon="account_circle" />
            <v-text-field label="Password" prepend-icon="lock" />
            <v-text-field label="E-mail" prepend-icon="contact_mail" />
            <v-text-field label="Birthday" prepend-icon="album" />
          </v-form>
        </v-card-text>
        <v-card-actions>
           <nuxt-link to="login">
             <v-btn color="info">
            กลับหน้า Login
          </v-btn>
           </nuxt-link>
          <v-spacer />
          <v-btn color="success">
            ยืนยันการสมัคร
          </v-btn>
        </v-card-actions>
      </v-card>
    </center>
    </v-card>
  </v-app>
</template>
