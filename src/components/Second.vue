<template>
    <h1>{{title}}</h1>
    <button @click.alt="clickListener">Change first color</button>
</template>



<script>
export default {
    props:['title'],
    methods:{
        clickListener(){
            this.$emit('changeColor')
        }
    }
}
</script>



<style scoped>
    h1{
        color: blue;
    }
</style>