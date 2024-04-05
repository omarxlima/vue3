<template>
  <Topo></Topo>

  <!-- <div v-show="showName">
    Nome: {{ name }}
    SobreNome: {{ lastName }}
  </div>

  <div v-if="accessLevel == 'admin'">Admin</div>
  <div v-else-if="accessLevel == 'marketing'"> Marketin</div>
  <div v-else>User</div> -->
  <!-- <h1 :class="classH1"> Curso de vue3 </h1> -->
  <h1 :class="styleClass"> Curso de vue3 </h1>

  <p :class="['text', {'title-home': isHome}]">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Suscipit sint consequatur deleniti 
    oluptas! Quos nihil dicta laudantium, accusamus, rem doloremque labore nostrum obcaecati impedit 
    quidem qui quam perspiciatis facilis quis.</p>

    <p :style="{ 'color': 'aqua', 'background-color': 'black' }" >Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odit nisi earum vel, dolor perferendis optio eaque quidem accusamus
       porro magni nobis molestias ad vitae! Repudiandae incidunt obcaecati in necessitatibus numquam.</p>



  <div>
    <div v-for="(todo, index) in todos" :key="todo.id">
      <img v-if="todo.imgSrc" :src="todo.imgSrc">
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
          "completed": false,
          "imgSrc": 'https://placehold.co/400'
        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false,
          "imgSrc": 'https://placehold.co/400'

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
      ],
      isHome : true,
      classH1:'title',
      pClass : 'text',
      styleClass: { 'color': 'aqua', backGroundColor: 'black' }

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
