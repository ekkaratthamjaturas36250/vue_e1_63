<template>
  <div>
    <h2>Hello {{ name }}</h2>
    <h2>Age {{ age }}</h2>
    <h2> Name:<input type="text" :value="name"></h2>
    <input type="text" v-model="name">

    <div>
      <button @click="doSave">
        Save
      </button>
    </div>
    <div>
      <button @click="doMenu">
        Main Menu
      </button>
    </div>
    <div>
      <button @click="doHome">
        Home
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Aekkarat Thiamjaturas',
      age: 19,
    }
  },
  methods: {
    doSave() {
      console.log('Do Save')
    },
    doHome() {
      this.$router.push('/')
    },
    doMenu() {
      this.$router.replace('menu')
    },
  },
}
</script>
