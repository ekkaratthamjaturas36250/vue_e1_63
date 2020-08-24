<template>
  <v-app id="app1">
    <v-container>
      <br>
      <center>
        <v-card width="420" color="#708090">
          <v-card-title>
            <h4>แสดง นร. นศ. ตามวิทยาลัย ผลการเรียนสูงกว่า 3.5</h4>
          </v-card-title>
          <v-card-text>
            <v-form>
              <v-text-field label="กรอกรหัสสถานศึกษา" prepend-icon="account_balance" v-model="school_id" />
            </v-form>
          </v-card-text>
          <v-card-text>
            <v-form>
              <v-text-field label="กรอก GPA" prepend-icon="account_balance" v-model="GPA" />
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
      <ul style="color:#000">
        <li v-for="st in student" :key="st.code">
          <span>{{ st.name }}</span>
          <span>{{ st.lastname }}</span>
          <span>{{ st.GPA }}</span>
          <span>{{ st.school_name }}</span>
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
      student: [
      ],
      showPassword: false,
      school_id: '',
      GPA: '',
    }
  },
  methods: {
    async doSave() {
      console.log('Save')
      console.log('user:', this.school_id)
      // this.$router.push('/register')
      let res = await fetch('http://localhost:7001/school6?school_id=' + this.school_id + '&GPA=' + this.GPA) // ส่งข้อมูลไป Server 7001
      // eslint-disable-next-line no-unused-vars
      let data = await res.json() // ส่งข้อมูลไป Server 7001
      console.log('data=', data.rows[0].GPA) // ใส่แสดงข้อมูลตรงหน้าจอ Serverเป็น rows:row จะใส่เป็น data.rows
      this.GPA = data.rows[0].GPA // ใส่แสดงข้อมูลตรงหน้าจอ Serverเป็น rows:row จะใส่เป็น data.rows
      this.student = data.rows[0]
    },
  },
}
</script>

<style>
 #app1 {
   background-image:linear-gradient(-225deg, #ffffff 0%, #dddddd 52%, #ffffff 100%);
}
</style>
