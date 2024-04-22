<template>

  <div>

    <BaseAlert v-if="showAlert" :variant="variant" @fechar="onClose()">
      {{ text }}

    </BaseAlert>

  </div>


</template>

<script>


import BaseAlert from '@/components/BaseAlert.vue'

export default {
  name: 'App',
  components: {
    BaseAlert
  },
  data() {
    return {
      showAlert: true,
      variant: 'success',
      text: 'seu formulário foi enviado com sucesso!'

    }
  },


  watch: {

  },

  computed: {

  },

  methods: {
    onClose() {
      this.showAlert = false
      console.log(' on close')
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
