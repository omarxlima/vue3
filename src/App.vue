<template>
  
  <div> 

    <div class="card">
      TEste
    </div>

    <BaseCard></BaseCard>
   
  </div>
    

</template>

<script>


import BaseCard from '@/components/BaseCard.vue'

export default {
  name: 'App',
  components: {
    BaseCard
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
