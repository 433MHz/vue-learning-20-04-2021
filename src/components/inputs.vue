<template>

    <input type="email" placeholder="email" v-model="email" @keyup="keyPressed"><br>
    <input type="text" placeholder="first name" v-model="firstName"><br>
    <input type="text" placeholder="second name" v-model="secondName"><br>

    <select v-model="option">
        <option value="first">first option</option>
        <option value="second">second option</option>
    </select><br>

    <input type="checkbox" v-model="checkbox" value="checkbox value">

    <h3>email: {{email}}</h3><br>
    <div v-for="emails in emailList" :key="emails">
       {{emails}} <button @click="removeFromList(emails)">remove</button>
    </div>
    <h3>first name: {{firstName}}</h3><br>
    <h3>second name: {{secondName}}</h3><br>
    <h3>option: {{option}}</h3><br>
    <h3>checkBox: {{checkbox}}</h3>

</template>

<script>
export default {
    data(){
        return{
            email: null,
            emailList: [],
            firstName: null,
            secondName: null,
            option: null,
            checkbox: []
        }
    },

    methods:{
        keyPressed(e){
            if(e.key === 'Enter' && this.email && !this.emailList.includes(this.email)){
                this.emailList.push(this.email),
                this.email = ''
            }
        },

        removeFromList(value){
            
            this.emailList = this.emailList.filter((current) => {if(current != value) return current})

        }
    }
}
</script>

<style>
    
</style>