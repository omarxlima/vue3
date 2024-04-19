<template>
  <Topo></Topo>


  <div>
      <input type="text" v-model="name"> <br>

      {{ name }}

      <br><br><br>

      <select v-model="pageCount" name="" id="">
          <option value="5">5</option>
          <option value="10">10</option>
          <option value="15">15</option>

      </select>

      <br> <br>

      {{  pageCount }}

      <br> <br>

      <input type="text" v-model="user.firstName"> <br>
      <input type="text" v-model="user.lastName"> <br>

      {{ user.firstName }} {{ user.lastName }}

      
    
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
        name : '',
        pageCount: 5,
        user: {
          firstName: '',
          lastName: '',
        }
    }
  },

  watch: {
      name(vl) {
        if(vl.length >=3) {
          this.saveUserName()
        }
      },
      pageCount() {
        this.changePage()
      },
      user: {
        handler() {
          console.log('user alterado')
        },
        deep:true
      }
  },

  computed: {
   
  },

  methods: {
    saveUserName() {
      console.log('ajax')
      console.log(this.name)
    },

    changePage() {
      console.log('ajax changePage')
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
