<template>
    <div>
        <h2>{{title}} - {{author}} - {{age}}</h2><br>

        <button v-on:click="age = age + 1"> Dodaj rok </button><br>
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
            this.age = this.age - 1;
        }
    }
}
</script>