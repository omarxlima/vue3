<template>
<div :class="BaseClass">
        <slot/>

        <button @click="onClick()">
            x
        </button>
</div>
</template>
<script>
    export default {
        // props: ['variant', 'test'],
        props: {
            variant: {
                type: String,
                default: ''
            },
           
        },

       
        computed: {
            BaseClass() {
                return ['alert', this.variant ? `alert-${this.variant}`: '' ]
            }
        },
        methods: {
            onClick() {
                this.$emit('fechar')
                console.log('clicou')
            }
        },
    }
</script>
<style>
    .alert{
        display: flex;
        justify-content: space-between;
        padding: 5px;
        border-radius: 6px;
        color: gray;
        background: #ddd;
    }
    
    .alert-success {
        background: #42b983;
        color: white;
    }
    .alert-danger {
        background: #f05151;
        color: white;
    }
</style>