<template>
  <Topo></Topo>

  <div>
    <!-- @ no logar da diretiva v-on  -->
    <button @click.once="onClick">
      Enviar
    </button>

  </div>

  <div @mouseover="onMouseover" @mouseout="onMouseOut">
    Mouse over

  </div>

  <form action="https://google.com" @submit.prevent="onSubmit">
      <input type="text" @keyup.enter="onKeyUp">
      <button type="submit"> Enviar</button>
  </form>


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



    }
  },

  methods: {
    onClick($event) {
      console.log('click', $event)
    },

    onMouseover($event) {
      console.log('mouse over', $event)
    },

    onMouseOut($event) {
      console.log('mouse out', $event)
    },
    onSubmit() {
      console.log('submit')
    },
    onKeyUp($event) {
      console.log('keyup', $event)
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
