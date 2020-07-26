<template>
    <v-app id="app1">
       <v-container class="text-center">
            <h1 id="fontcolor" class="mt-12">Welcome!</h1>
            <span id="fontcolor1">Lorem ispansum dolor sit amet,</span><br>
            <span id="fontcolor1"> consectetur adopiscing elit.</span>
            
            

            <div class="boximg mt-10">
                <img width="300px;" height="340px;" style="margin-top: -20px;" src="https://www.img.in.th/images/37608065c355f626c505bf5d098ba014.md.jpg">
            </div>

       </v-container>

        <v-container class="text-center mt-15">
            <a href="#/work2"><v-btn round color="primary" width="320px" >Sign in</v-btn></a>
        </v-container>

    </v-app>
</template>

<script>
export default {
    layout:'them',
}
</script>

<style>
 #app1 {
   background-image:linear-gradient(-225deg, #ffffff 0%, #ffffff 52%, #ffffff 100%);
}
#fontcolor {
    color:#696969;
}
#fontcolor1 {
    color:#BEBEBE;
}
.boximg {
    background-color: #BEBEBE;
    width: 350px;
    height: 300px;

}
</style>
