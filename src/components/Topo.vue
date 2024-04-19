<template>
    <header class="header">
        Header
    </header>

</template>


<script>
export default {
    mounted() {
        window.addEventListener('resize', this.resize)
    },



    beforeUnmount() {
        //destruir eventos
        //listeners
        //libs
        console.log('before unmount')
        
    },

    unmounted() {
        console.log('unmounted')
      
    },

    methods: {
        resize($e) {
            console.log($e)
        }
    }
}
</script>

<style>
.header {
    background: #000;
    color: #fff;
}
</style>