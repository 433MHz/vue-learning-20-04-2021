<template>
<div id="container">
    <h1>Reaction timer</h1>    
    <button @click="start" :disabled="isPlaying">play</button><br>
    <block :delay="delay" v-if="isPlaying" @reactionTime="emitedFromBlock($event)"></block>
    <result :timer="timer" v-if="!isPlaying"></result>
</div>
</template>


<script>
import Block from './components/Block.vue'
import Result from './components/Result.vue'
export default {
  components: {Block, Result },
  data(){
    return{
      isPlaying: false,
      delay: null,
      timer: null,
    }
  },

  methods:{
    start(){
      this.isPlaying = true,
      this.delay = 2000 + Math.random() * 5000
    },

    emitedFromBlock(timer){
      this.timer = timer,
      this.isPlaying = false
    }
  }
}
</script>



<style scoped>
  #container{
    text-align: center;
    font-size: 20px;
    margin-top: 70px;
  }
</style>