<template>
  <Topo v-if="showHeader"/>

    <div v-show="showName"> 
      Nome: {{ name }}
      SobreNome: {{ lastName }}
    </div>

    <div v-if="accessLevel == 'admin'">Admin</div>
    <div v-else-if="accessLevel == 'marketing'"> Marketin</div>
    <div v-else >User</div>



  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

import Topo from './components/Topo.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Topo
  },
  data() {
    return {
      showHeader: false,
      name : 'Luke',
      lastName: 'Skywalker',
      showName: true,
      accessLevel: 'outro'
    }
  },
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
