<template>
  <form id="empployee-form">
    <label>Employee name</label>
    <input type="text" />
    <label>Employee Email</label>
    <input type="text" />
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
  }
</script>

<style scoped>
  form {
    margin-bottom: 2rem;
  }
</style>