<template>
  <v-app id="app1">
    <v-container>
      <br>
      <center>
        <v-card width="420" color="#708090">
          <v-card-title>
            <h3>ค้นหาชื่อนักเรียนว่าอยู่วิลัยไหน  </h3>
            <h4 style="text-align:center; color:#FF6347;">
              {{ school_n }}
            </h4>
          </v-card-title>
          <v-card-text>
            <v-form>
              <v-text-field label="กรอกรหัสนักศึกษา" prepend-icon="account_balance" v-model="student_id" />
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
    </v-container>
  </v-app>
</template>

<script>
export default {
  layout: 'them4',
  name: 'App',
  data () {
    return {
      showPassword: false,
      student_id: '',
      school_n: '',
    }
  },
  methods: {
    async doSave() {
      console.log('Save')
      console.log('user:', this.student_id)
      // this.$router.push('/register')
      let res = await fetch('http://localhost:7001/school_n?student_id=' + this.student_id) // ส่งข้อมูลไป Server 7001
      // eslint-disable-next-line no-unused-vars
      let data = await res.json() // ส่งข้อมูลไป Server 7001
      console.log('data=', data.rows[0].school_name) // ใส่แสดงข้อมูลตรงหน้าจอ Serverเป็น rows:row จะใส่เป็น data.rows
      this.school_n = data.rows[0].school_name // ใส่แสดงข้อมูลตรงหน้าจอ Serverเป็น rows:row จะใส่เป็น data.rows
    },
  },
}
</script>

<style>
 #app1 {
   background-image:linear-gradient(-225deg, #ffffff 0%, #dddddd 52%, #ffffff 100%);
}
</style>
