<template>
    <h1 ref="title">{{title}}</h1><br>

    <input type="text" placeholder="Change title" ref="input"><br>

    <button @click="focusOnInput">Focus on input field</button><br>
    <button @click="makeTitleBlue">Make title blue</button><br>
    <button @click="makeTitleSalmon">Make title salmon</button>
</template>


<script>
export default {
    data(){
        return{
            title: 'Title'
        }
    },

    methods:{
        focusOnInput(){
            this.$refs.input.focus()
        },

        makeTitleSalmon(){
            this.$refs.title.classList.add('second')
            this.$refs.title.classList.remove('first')
        },

        makeTitleBlue(){
            this.$refs.title.classList.add('first')
            this.$refs.title.classList.remove('second')
        }
        }
}
</script>


<style>

    .first{
        color: lightskyblue;
    }

    .second{
        color: lightsalmon;
    }
</style>