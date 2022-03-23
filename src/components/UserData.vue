<template>
  <section>
    <form @submit.prevent="sendData">
      <label>name</label>
      <input type="text" v-model="enteredName" />
      <label>Age</label>
      <input type="text" v-model="enteredAge" />
      <button>Enter Data</button>
    </form>
  </section>
</template>

<script>
export default {
  emits: ['form-data'],
  data() {
    return {
      enteredName: "",
      enteredAge: "",
    };
  },
  methods: {
    sendData() {
      this.$emit('form-data', this.enteredName, this.enteredAge);
    },
  },
};
</script>

<style>
</style>