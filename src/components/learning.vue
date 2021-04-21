<template>
    <div>
        <div v-for="book in books" :key="book.title">
            <div class="bookDiv" v-if="showBooks" :class="{bookDivFav: book.isFav}" @click="book.isFav = !book.isFav">
                <div>
                    <h3>{{book.title}}</h3> <h5> writen by: {{book.author}}</h5>
                </div>
            </div>
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
                {title: 'Hyperion', author: 'Daniel Simon', isFav: true},
                {title: 'Robinson Cruzoe', author:'Daniel Defoe', isFav: false},
                {title: 'Vue', author:'Vue maker', isFav: true}
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

    #bottomDiv{
        margin-top: 400px;
    }

    .bookDiv{
        background-color: lightgray;
        width: 500px;
        display: inline-block;
        height: 100px;
        margin: 10px;
        border-radius: 10px;
    }

    .bookDivFav{
        background-color: lightgreen;
        width: 500px;
        display: inline-block;
        height: 100px;
        margin: 10px;
        border-radius: 10px;
    }
</style>