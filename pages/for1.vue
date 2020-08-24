/* eslint-disable no-unused-vars */
<template>
  <div>
    <h1>Student List</h1>
    <v-container>
      <v-data-table
        :headers="headers"
        :items="student"
        :items-per-page="5"
        class="elevation-1"
      />
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      headers: [/* script table */
        {
          text: 'รหัสนักศึกษา',
          align: 'start',
          sortable: false,
          value: 'student_id',
        },
        { text: 'ชื่อ', value: 'name' },
        { text: 'สกุล', value: 'lastname' },
        { text: 'GPA', value: 'GPA' },
      ],

      student: [
      ],
    }
  },
  created() {
    this.listStudent()
  },
  methods: {
    async listStudent() {
      console.log('List Std')
      let res = await fetch('http://localhost:7001/liststd')
      // eslint-disable-next-line no-unused-vars
      let data = await res.json() // ส่งข้อมูลไป Server 7001
      console.log('data', data.rows[0])
      this.student = data.rows[0]
    },
  },
}
</script>
