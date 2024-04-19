<template>
  <Topo v-if="showTopo"/>

<!-- el component raiz -->
  <div> 
      
      <h1> adfasdf</h1>

      <input type="text" v-model="name">

      {{ name }} <br><br>

      <button @click="showTopo = !showTopo">
          ativar e desativar topo
      </button>
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
       name: 'Lima Marx',
       showTopo: true
    }
  },

  //criação
      // preparar o componente
      //ajax, inicializar variaveis
     //Não tem acesso ao DOM
  //montagem
      //Inicializar uma lib externa (new Lib())
      //tem acesso ao DOM
  //atualização 
      //DEBUG
  //desmontagem

      //remover tudo que vai consumir memória (lib->destroy)
  
  //hooks

  // beforeUpdate(){
  //   console.log('before update', this.name)
  // },
  // updated() {
  //   console.log('updated', this.name)
  // },
// beforeCreate(){
//   console.log('before create')
//   console.log('Estado:', this.name)
//   console.log('DOM:', this.$el)

// },
// created() {
//   console.log('created')
//   console.log('Estado:', this.name)
//   console.log('DOM:', this.$el)


// },
// beforeMount() {
//   console.log('before mount')
//   console.log('Estado:', this.name)
//   console.log('DOM:', this.$el)


// },
// mounted() {
//   console.log('mounted')
//   console.log('Estado:', this.name)
//   console.log('DOM:', this.$el)

  
// },



  watch: {
      
  },

  computed: {
   
  },

  methods: {
   

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
