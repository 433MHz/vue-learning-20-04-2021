<template>
    <div>
        <h2 v-if="showBooks">{{title}} - {{author}} - {{age}}</h2><br>

        <button v-on:click="age++"> Dodaj rok </button><br>
        <button v-on:click="removeOneYear">Odejmij rok</button><br>
        <button v-on:click="toogleBooks"><span v-if="showBooks === false">Show books</span> <span v-if="showBooks === true">Hide books</span></button>
    </div>
</template>




<script>
export default {
    data(){
        return{
            showBooks: true,
            title: 'tytuł książki',
            author: 'autor książki',
            age: 45
        }
    },

    methods:{
        removeOneYear(){
            this.age --;
        },

        toogleBooks(){
            this.showBooks = !this.showBooks
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