<template>
  <Topo></Topo>


  <div>
    
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
     
    }
  },

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
