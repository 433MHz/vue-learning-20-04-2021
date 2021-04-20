<template>
    <div>
        <div v-for="book in books" v-bind:key="book.title">
            <h2 v-show="showBooks">{{book.title}} - {{book.author}}</h2><br>
        </div>
       
        <button v-on:click="toogleBooks"><span v-if="!showBooks">Show books</span> <span v-else>Hide books</span></button><br>

    </div>
</template>




<script>
export default {
    data(){
        return{
            showBooks: true,

            books:[
                {title: 'Hyperion', author: 'Daniel Simon'},
                {title: 'Robinson Cruzoe', author:'Daniel Defoe'},
                {title: 'Vue', author:'Vue maker'}
            ]
        }
    },

    methods:{
        removeOneYear(){
            this.age --;
        },

        toogleBooks(){
            this.showBooks = !this.showBooks
        },
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