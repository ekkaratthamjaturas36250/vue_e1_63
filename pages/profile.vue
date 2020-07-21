<template>
    <div class="my-15">
    
<v-card
    max-width="400"
    class="mx-auto"
  >

    <v-container>
      <v-row dense>
        <v-col cols="12">
            
          <v-card
            color="#528B8B" 
          >
            <span class="my-5"></span>
            <center><v-avatar class="my-2" size="120"><img width="120" height="60" src="https://scontent.fbkk12-2.fna.fbcdn.net/v/t1.0-9/s960x960/80608518_2765786090155210_9048337477999263744_o.jpg?_nc_cat=104&_nc_sid=110474&_nc_eui2=AeFModcfmRbv4TNhLjdBw-E7D6ZgrxWPL7wPpmCvFY8vvGDfOY6PoxBvKXrO-laNd_fvJWRaptSI_v18ImMri9r1&_nc_ohc=eSFzXSWLKLQAX8mqprm&_nc_ht=scontent.fbkk12-2.fna&_nc_tp=7&oh=ad6b4771398e915a66ee9b86eccca6b3&oe=5F3D8813"></v-avatar></center>
             <center><v-btn btn>Change image</v-btn></center>
            <center><span>Mr. AEKKARAT THIAMJATURAS</span></center>
            <center><h2>Infomation Technology</h2></center>
            <v-card-subtitle>Birthday: 23 July 2000.
                            <br>Facebook: Fluke Thaimjaturat
                            <br>Line: 526631
                            <br>- Nothing kills you like your mind -</v-card-subtitle>
          </v-card>
        </v-col>

        <v-col
          v-for="(item, i) in items"
          :key="i"
          cols="12"
        >
          <v-card
            :color="item.color"
            dark
          >
            <div class="d-flex flex-no-wrap justify-space-between">
              <div>
                <v-card-title
                  class="headline"
                  v-text="item.title"
                ></v-card-title>

                <v-card-subtitle v-text="item.artist"></v-card-subtitle>
              </div>

              <v-avatar
                class="ma-3"
                size="125"
                tile
              >
                <v-img :src="item.src"></v-img>
              </v-avatar>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>

  </v-card>


      
    </div>
</template>

<script>
export default {
  layout:"defaultprofile",
}
</script>
