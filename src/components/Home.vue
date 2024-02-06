<template>
<div class="container">
  <h2>List Users</h2>
  <table class="table">
    <thead>
    <tr>
      <th scope="col">ID</th>
      <th scope="col">Name</th>
      <th scope="col">Age</th>
      <th scope="col">Action</th>
    </tr>
    </thead>
    <tbody>
    <tr v-for="(user, index) in users" :key="index">
      <th scope="row">{{ index +1 }}</th>
      <td>{{ user.name }}</td>
      <td>{{ user.age }}</td>
      <td><button v-on:click="deleteUser(user.id)">
        Delete
      </button></td>
    </tr>
    </tbody>
  </table>
</div>
</template>

<script>
export default {
  name: "HOME",
  props:['users'],
  methods:{
    deleteUser(id){
      this.$emit('delete',{id})
    }
  }
}
</script>

<style scoped>

</style>