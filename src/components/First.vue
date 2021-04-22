<template>
    <h1 :class="{red: theme, blue: !theme}">{{title}}</h1>
</template>



<script>
export default {
    props:['title', 'theme']
}
</script>



<style scoped>
    h1{
        color: aquamarine;
    }

    .red{
        color: red;
    }

    .blue{
        color: blue;
    }
</style>