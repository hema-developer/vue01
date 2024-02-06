<template>
  <div id="app" class="container-fluid">
    <NavBar/>
    <Home :users="users" @delete="deleteUser"/>
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Home from './components/Home.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    Home
  },
  data() {
    return {
      users: [
        {id: 1, name: "Ibrahim Samir", age: 35},
        {id: 2, name: "Ahmed samir", age: 28},
        {id: 3, name: "Yasin Ibrahim", age: 10},
        {id: 4, name: "Mohammed Syed", age: 4},
        {id: 5, name: "Yasser Ibrahim", age: 20},
        {id: 6, name: "Yasser Ibrahim", age: 20},
        {id: 7, name: "Yasser Ibrahim", age: 20},
        {id: 8, name: "Yasser Ibrahim", age: 20},
        {id: 9, name: "Yasser Ibrahim", age: 20},
        {id: 10, name: "Yasser Ibrahim", age: 20},
      ]
    }
  }, methods: {
    deleteUser(id) {
      this.users = this.users.filter(user => {
        return user.id != id.id;
      })
    }
  }
}
</script>
