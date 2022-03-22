<template>
  <form @sumbit.prevent="sendData">
      <label>Username</label>
      <input type="text" v-model="username"/>
      <label>Age</label>
      <input type="number" v-model="age"/>
  </form>
</template>

<script>
export default {
    data() {
        return {
            username: '',
            age: ''
        }
    },
    methods: {
        sendData() {
            this.$emit('form-data', this.username, this.age)
        }
    }
}
</script>

<style>

</style>