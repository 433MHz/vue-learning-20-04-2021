<template>
    <div>
        <h2 v-if="age > 45">{{title}} - {{author}} - {{age}}</h2><br>

        <button v-on:click="age++"> Dodaj rok </button><br>
        <button v-on:click="removeOneYear()">Odejmij rok</button>
    </div>
</template>




<script>
export default {
    data(){
        return{
            title: 'tytuł książki',
            author: 'autor książki',
            age: 45
        }
    },

    methods:{
        removeOneYear(){
            this.age --;
        }
    }
}
</script>

<style>
    #capitalMaker{
        width: 100px;
        height: 50px;
        background-color: azure;
    }
</style>