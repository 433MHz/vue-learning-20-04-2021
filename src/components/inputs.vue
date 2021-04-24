<template>
  <form>

    <input type="email" placeholder="email" v-model="email"><br>
    <input type="text" placeholder="first name" v-model="firstName"><br>
    <input type="text" placeholder="second name" v-model="secondName"><br>

    <select v-model="option">
        <option value="first">first option</option>
        <option value="second">second option</option>
    </select><br>

    <input type="checkbox" v-model="checkbox" value="checkbox value">

    <h3>email: {{email}}</h3><br>
    <h3>first name: {{firstName}}</h3><br>
    <h3>second name: {{secondName}}</h3><br>
    <h3>option: {{option}}</h3><br>
    <h3>checkBox: {{checkbox}}</h3>

  </form>
</template>

<script>
export default {
    data(){
        return{
            email: null,
            firstName: null,
            secondName: null,
            option: null,
            checkbox: []
        }
    }
}
</script>

<style>

</style>