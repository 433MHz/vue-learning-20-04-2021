<template>
  <div id="container">
    <first :title="titleFirst" v-if="showFirst"> 
      <h2>Here i'm sending data to this component from parent</h2>
    </first><br>
    <first v-if="showSecond" :title="titleSecond">
      <h2>Here i'm making same thing</h2>
    </first><br>
    <button @click="showSecond = !showSecond">Second toogle</button><br>
    <button @click="showFirst = !showFirst">First toogle</button><br>

    <div id="forTeleport"></div>

    <teleport to="#forTeleport">
      <h3>I'm going to be teleported</h3>
    </teleport>
  </div>
</template>


<script>
import First from './components/First.vue'

export default {
  components: {First },
  
  data(){
    return{
      titleFirst: 'First component',
      titleSecond: 'Second component',
      showSecond: false,
      showFirst: false
    }
  },

  methods:{
    toggleFirstComponent(data){
      this.titleFirst = data
    },

    toggleSecondComponent(data){
      this.titleSecond = data
    }
  }
}

</script>



<style scoped>
#container{
  text-align: center;
  color: white;
}
</style>