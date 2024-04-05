<template>
  <Topo></Topo>
  <div>

    <button @click="click"> Click</button>

    {{ nomeCompleto }}
  </div>
  <br> <br>
  

  <h2>Todos Incompletos</h2>
  <div v-for="todo in naoConcluido" :key="todo.id">

    {{ todo.title }}

  </div>

  <h2>Todos Completas</h2>
  <div v-for="todo in concluido" :key="todo.id">

    {{ todo.title }}

  </div>
  <br><br>
  <h2>Todos </h2>
  <div v-for="todo in todos" :key="todo.id">

    <input type="checkbox" v-model="todo.completed">
    {{ todo.title }}

  </div>

</template>

<script>


import Topo from './components/Topo.vue'

export default {
  name: 'App',
  components: {
    Topo
  },
  data() {
    return {
      user: {
        name: 'Karl',
        lastName: 'Marx'
      },
      todos: [
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
        },
        {
          "userId": 1,
          "id": 6,
          "title": "qui ullam ratione quibusdam voluptatem quia omnis",
          "completed": false
        },
        {
          "userId": 1,
          "id": 7,
          "title": "illo expedita consequatur quia in",
          "completed": false
        },
        {
          "userId": 1,
          "id": 8,
          "title": "quo adipisci enim quam ut ab",
          "completed": true
        },
      ]
    }
  },
  computed: {
    nomeCompleto() {
      return `${this.user.name} ${this.user.lastName} `
    },

    naoConcluido() {
      return this.todos.filter(todo => !todo.completed)
    },
    concluido() {
      return this.todos.filter(todo => todo.completed)

    }
  },

  methods: {

    click() {
      console.log(this.nomeCompleto)
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


.title {
  font-size: 20px;
  color: blue;
}

.title-home {
  font-size: 40px;
  color: green;
}

.text {
  color: blueviolet;
}
</style>
