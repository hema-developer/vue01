<template>
<div class="container">
  <h2>List Users</h2>
  <table class="table">
    <thead>
    <tr>
      <th scope="col">ID</th>
      <th scope="col">Name</th>
      <th scope="col">Age</th>
    </tr>
    </thead>
    <tbody>
    <tr v-for="user in users" :key="user.id">
      <th scope="row">{{ user.id }}</th>
      <td>{{ user.name }}</td>
      <td>{{ user.age }}</td>
    </tr>
    </tbody>
  </table>
</div>
</template>

<script>
export default {
  name: "HOME",
  data (){
    return {
      users :[
          {
            id: 1,
            name: "Ibrahim Samir",
            age: 35
          },
          {
            id: 2,
            name: "Ahmed samir",
            age: 28
          },
          {
            id: 3,
            name: "Yasin Ibrahim",
            age: 10
          },
        {
          id: 4,
          name: "Mohammed",
          age: 4
        },
        {
          id: 5,
          name: "Ysaaer",
          age: 20
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>