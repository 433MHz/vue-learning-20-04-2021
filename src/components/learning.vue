<template>
    <div>
        <h2 v-show="showBooks">{{title}} - {{author}} - {{age}}</h2><br>

        <button v-on:click="age++"> Dodaj rok </button><br>
        <button v-on:click="removeOneYear">Odejmij rok</button><br>
        <button v-on:click="toogleBooks"><span v-if="!showBooks">Show books</span> <span v-else>Hide books</span></button><br>

        <h1>{{actually}}</h1>

        <div class="box" @mouseenter="changeActually('mouse entered on div 1')">mouseover (enter)</div>
        <div class="box" @mouseleave="changeActually('mouse leaved div 2')">mouseover(leave)</div>
        <div class="box" @dblclick="changeActually('double clicked div 3')">double click</div>
        <div class="box" @mousemove="mouseMove">{{mouseX}} - {{mouseY}}</div>
    </div>
</template>




<script>
export default {
    data(){
        return{
            showBooks: true,
            title: 'tytuł książki',
            author: 'autor książki',
            age: 45,
            actually: '',
            mouseX: 1,
            mouseY: 1
        }
    },

    methods:{
        removeOneYear(){
            this.age --;
        },

        toogleBooks(){
            this.showBooks = !this.showBooks
        },

        changeActually(actually){
            this.actually = actually
        },

        mouseMove(move){
            this.mouseX = move.offsetX,
            this.mouseY = move.offsetY
            this.actually = this.mouseX + " - " + this.mouseY
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

    .box{
        width: 400px;
        padding: 25px;
        margin: 50px;
        height: 200px;
        background-color: lightgray;
        display: inline-block;
    }
</style>