<template>
    <h1>{{title}}</h1>

    <slot>This is default empty slot</slot>
</template>



<script>
export default {
    props:['title']
}
</script>



<style scoped>
    
</style>