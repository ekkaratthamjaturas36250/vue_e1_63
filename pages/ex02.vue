<template>
  <div>
    <h1>Hello {{ name }} <br> Age:{{ age }}</h1>
    <br>
     <v-text-field
            v-model="first"
            label="กรุณากรอกชื่อ"
            placeholder="กรุณากรอกชื่อของท่าน"
            outlined
            loading
            shaped
          >
    </v-text-field>

     <v-text-field 
            v-model="first"
            label="Your Name"
            filled
            dense
          ></v-text-field>

         <v-text-field
            outlined
            label="Append"
            append-icon="mdi-map-marker"
          ></v-text-field>
  </div>
</template>

<script>
export default {
    data: () => ({
    name:"Aekkarat",
    age:19,
    dep:"Information Technology",
    first:"Chaiyaphum"
})
}
</script>

