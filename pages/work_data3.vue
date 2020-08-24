<template>
  <v-app id="app1">
    <v-container>
      <br>
      <center>
        <v-card width="420" color="#708090">
          <v-card-title>
            <h4>แสดงชื่อผู้หญิงทั้งหมด พร้อมแสดงวิลัย</h4>
          </v-card-title>
          <v-card-text>
            <v-form>
              <v-text-field label="กรอกรหัสวิลัย" prepend-icon="account_balance" v-model="school_id" />
            </v-form>
          </v-card-text>
          <v-card-actions>
            <v-spacer />
            <v-btn color="success" @click="doSave">
              ค้นหา
            </v-btn>
          </v-card-actions>
        </v-card>
      </center>
      <br>
      <ul style="color:#000;">
        <li v-for="nc in name_coll" :key="nc.code">
          <span>{{ nc.name }}</span>
          <span>{{ nc.lastname }}</span>
          <span>{{ nc.gender }}</span>
          <span>{{ nc.school_name }}</span>
        </li>
      </ul>
    </v-container>
  </v-app>
</template>

<script>
export default {
  layout: 'them4',
  name: 'App',
  data () {
    return {
      name_coll: [
      ],
      showPassword: false,
      school_id: '',
      school_n: '',
    }
  },
  methods: {
    async doSave() {
      console.log('Save')
      console.log('user:', this.school_id)
      // this.$router.push('/register')
      let res = await fetch('http://localhost:7001/female?school_id=' + this.school_id) // ส่งข้อมูลไป Server 7001
      // eslint-disable-next-line no-unused-vars
      let data = await res.json() // ส่งข้อมูลไป Server 7001
      console.log('data=', data.rows[0].school_name) // ใส่แสดงข้อมูลตรงหน้าจอ Serverเป็น rows:row จะใส่เป็น data.rows
      this.school_n = data.rows[0].school_name // ใส่แสดงข้อมูลตรงหน้าจอ Serverเป็น rows:row จะใส่เป็น data.rows
      this.name_coll = data.rows[0]
    },
  },
}
</script>

<style>
 #app1 {
   background-image:linear-gradient(-225deg, #ffffff 0%, #dddddd 52%, #ffffff 100%);
}
</style>
