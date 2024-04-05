<template>
  <Topo></Topo>

  <!-- <div v-show="showName">
    Nome: {{ name }}
    SobreNome: {{ lastName }}
  </div>

  <div v-if="accessLevel == 'admin'">Admin</div>
  <div v-else-if="accessLevel == 'marketing'"> Marketin</div>
  <div v-else>User</div> -->
  <!-- <h1 :class="classH1"> Curso de vue3 </h1> 
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
-->

<div>
  <div>
    One-way data binding

    Two-way data binding
    v-model -> formulários
    <br>
    <br>

   <div>
    <label for="nome"> Nome:</label> <br>
    <input type="text" v-model="nome">
    <br>
    {{ nome }}

    <br>
    <br>
    <label for="">Estados:</label> <br>
    <select v-model="estados">
        <option value="">Selecione</option>
        <option value="Maranhão">Maranhão</option>
        <option value="Rio de Janeiro">Rio de Janeiro</option>
        <option value="São Paulo">São Paulo</option>

    </select> <br> <br>

    {{  estados }}

    <div>
      <label for=""> newsLetter</label>
      <input  v-model="newsletter" type="radio" value="Sim"> Sim 
      <input  v-model="newsletter" type="radio" value="Não"> Não
      <br> <br>

      {{ newsletter }}

      <br> <br>

      


    </div>


   </div>

    <!-- <br> -->

    <!-- {{ nome }} -->

  </div>
</div>





</template>

<script>


import Topo from './components/Topo.vue'

export default {
  name: 'App',
  components: {
  //   /* HelloWorld,
    Topo
  },
  data() {
    return {
      nome : 'Karl Marx',
      estados: '',
      newsletter: 'Sim',
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
      styleClass: { 'color': 'aqua', backGroundColor: 'black' },
     

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
