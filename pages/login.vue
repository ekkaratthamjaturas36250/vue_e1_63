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
            <v-text-field label="Username" prepend-icon="account_circle" v-model="user" /><v-text-field
              :type="showPassword ? 'text' : 'password'"
              label="Password"
              v-model="password"
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
          <v-btn color="success" @click="doSave">
            Login
          </v-btn>
        </v-card-actions>
      </v-card>
    </center>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      showPassword: false,
      user: '',
      password: ''
    }
  },
  methods:{
   async doSave(){
      console.log("Save")
      console.log("user:", this.user)
      console.log("password:", this.password)
      this.$router.push('/register')
      let res = await fetch('http://localhost:7001/list?user='+this.user) //ส่งข้อมูลไป Server 7001
      let data = await res.json()                                         //ส่งข้อมูลไป Server 7001
    }
  },
}
</script>
