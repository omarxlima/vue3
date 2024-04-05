<template>
  <Topo></Topo>

  <!-- <div v-show="showName">
    Nome: {{ name }}
    SobreNome: {{ lastName }}
  </div>

  <div v-if="accessLevel == 'admin'">Admin</div>
  <div v-else-if="accessLevel == 'marketing'"> Marketin</div>
  <div v-else>User</div> -->

  <div>
    <div v-for="(todo, index) in todos" :key="todo.id">
     {{ index }} - {{ todo.title }}
    </div>

  </div>



  <HelloWorld />
</template>

<script>


import Topo from './components/Topo.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Topo
  },
  data() {
    return {
      // showHeader: true,
      // name: 'Luke',
      // lastName: 'Skywalker',
      // showName: true,
      // accessLevel: 'admin',
      todos: [
        {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false
        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false
        },
        {
          "userId": 1,
          "id": 3,
          "title": "fugiat veniam minus",
          "completed": false
        },
        {
          "userId": 1,
          "id": 4,
          "title": "et porro tempora",
          "completed": true
        },
        {
          "userId": 1,
          "id": 5,
          "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
          "completed": false
        }
      ]
    }

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
