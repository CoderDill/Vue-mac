<template>
  <form>
      <label>Name</label>
      <input type="text" v-model="name"/>
      <label>Age</label>
      <input type="number" v-model="age"/>
  </form>
</template>

<script>
export default {
    data() {
        return {
            name: '',
            age: ''
        }
    }
}
</script>

<style>

</style>