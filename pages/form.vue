<template>
  <v-form
    ref="form"
    v-model="valid"
    lazy-validation
  >
    <v-text-field
      v-model="std_id"
      :counter="10"
      label="Student_ID"
      required
    />

    <v-text-field
      v-model="name"
      label="Name"
      required
    />

    <v-text-field
      v-model="lastname"
      :counter="10"
      label="Lastname"
      required
    />

    <v-text-field
      v-model="gpa"
      :counter="10"
      label="GPA"
      required
    />
    <v-btn
      color="error"
      class="mr-4"
      @click="reset"
    >
      Reset Form
    </v-btn>
  </v-form>
</template>

<script>
export default {
  data: () => ({
    user: '4922010029',
    std_id: '',
    valid: true,
    name: '',
    lastname: '',
    gpa: '',
    nameRules: [
      v => !!v || 'Name is required',
      v => (v && v.length <= 10) || 'Name must be less than 10 characters',
    ],
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
    ],
    select: null,
    items: [
      'Item 1',
      'Item 2',
      'Item 3',
      'Item 4',
    ],
    checkbox: false,
  }),
  created() {
    // eslint-disable-next-line no-undef
    this.init_load()
  },
  methods: {
    async init_load() {
      console.log('Welcome')
      // this.$router.push('/register')
      let res = await fetch('http://localhost:7001/list1?user=' + this.user) // ส่งข้อมูลไป Server 7001
      // eslint-disable-next-line no-unused-vars
      let data = await res.json() // ส่งข้อมูลไป Server 7001
      console.log('data=', data.rows[0].GPA) // ใส่แสดงข้อมูลตรงหน้าจอ Serverเป็น rows:row จะใส่เป็น data.rows
      this.gpa = data.rows[0].GPA // ใส่แสดงข้อมูลตรงหน้าจอ Serverเป็น rows:row จะใส่เป็น data.rows
      this.name = data.rows[0].name
      this.lastname = data.rows[0].lastname
      this.std_id = data.rows[0].student_id
    },
  },
}
</script>
