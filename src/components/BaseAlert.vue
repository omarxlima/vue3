<template>
<div :class="BaseClass">

    {{ test }}
        <slot/>
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
            test: {
                type: String,
                default: 'test'
            }
        },

        mounted() {
            console.log(this.test)
        },
        computed: {
            BaseClass() {
                return ['alert', this.variant ? `alert-${this.variant}`: '' ]
            }
        }
    }
</script>
<style>
    .alert{
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