/* eslint-disable no-unused-vars */
<template>
  <div>
    <h1>Student List</h1>
    <ul>
      <li v-for="st in student" :key="st.code">
        <span>{{ st.name }}</span>
        <span>{{ st.lastname }}</span>
        <span>{{ st.GPA }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      student: [
      ],
    }
  },
  methods: {
    async listStudent() {
      console.log('List Std')
      let res = await fetch('http://localhost:7001/liststd')
      // eslint-disable-next-line no-unused-vars
      let data = await res.json() // ส่งข้อมูลไป Server 7001
      console.log('data',data.rows[0])
      this.student = data.rows[0]
    },
  },
  created() {
    this.listStudent()
  },
}
</script>
