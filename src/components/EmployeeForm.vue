<template>
  <form id="employee-form" @submit.prevent="handleSubmit">
    <label>Employee name</label>
    <input v-model="employee.name" type="text" />
    <label>Employee Email</label>
    <input v-model="employee.email" type="text" />
    <button>Add Employee</button>
  </form>
</template>

<script>
  export default {
    name: 'employee-form',
    data() {
      return {
        employee: {
          name: '',
          email: '',
        },
      }
    },
    methods: {
      handleSubmit() {
        console.log('posting')
        this.$emit('add:employee', this.employee)
      },
    },
  }
</script>

<style scoped>
  form {
    margin-bottom: 2rem;
  }
</style>