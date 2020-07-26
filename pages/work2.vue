<template>
    <v-app id="app1">
        <v-container class="text-center" id="app2">
                <v-icon class="mt-10" color="#1E90FF" style="font-size:100px;">mdi-account-circle</v-icon>
                <br>
                <br>
                <br>
        </v-container>
        <v-card style="background-color:#ffffff; margin: 20px;">
          <v-container style="background-color: #1E90FF;">
              
      
     <v-card-text>
          <v-form>
            <v-text-field color="#ffffff" label="Username" />
         <v-text-field color="#ffffff" label="Password" type="password" />
          </v-form>

    <v-row>
        <v-col cols="6">
        <v-checkbox color="#ffffff;" label="Remember me"></v-checkbox>  
        </v-col>
     <v-col cols="6">
         <br>
        <span>Forgot Password ?</span>
    </v-col>
    </v-row>
        </v-card-text>
    
          </v-container>
        </v-card>

        <v-container class="text-center mt-3">
            <a href="#/work3"><v-btn round color="primary" width="320px" >Sign in</v-btn></a>
        </v-container>

    </v-app>
</template>
<script>
export default {
    layout:'them2',
}
</script>

<style>
 #app1 {
   background-image:linear-gradient(-225deg, #F5F5F5 0%, #F5F5F5 52%, #F5F5F5 100%);
}
 #app2 {
   background-image:linear-gradient(-225deg, #F5F5F5 0%, #F5F5F5 52%, #F5F5F5 100%);
}

</style>


