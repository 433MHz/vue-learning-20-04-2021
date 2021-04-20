<template>
    <div>
        <div v-for="book in books" v-bind:key="book.title">
            <h2 v-show="showBooks">{{book.title}} - {{book.author}}</h2><br>
        </div>
       
        <button v-on:click="toogleBooks"><span v-if="!showBooks">Show books</span> <span v-else>Hide books</span></button><br>
        <button @click="toggleLink">
            <span v-if="link3 === link2">Youtube</span> 
            <span v-else-if="link3 === link1">Google</span>
            <span v-else>Unknown site</span>
        </button><br>

        <a v-bind:href = link3>link</a>
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
            ],

            link1: 'https://www.google.pl/',
            link2: 'https://www.youtube.com/',
            link3: this.link1
        }
    },

    methods:{
        removeOneYear(){
            this.age --;
        },

        toogleBooks(){
            this.showBooks = !this.showBooks
        },

        toggleLink(){
            if(this.link3 === this.link1){
                this.link3 = this.link2
            }
            else if(this.link3 === this.link2){
                this.link3 = this.link1
            }
            else{
                this.link3 = this.link1
            }
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