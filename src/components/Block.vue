<template>
  <div class="block" v-if="showBlock" @click="stopTimer">
      click me
  </div>
</template>

<script>
export default {
    props: ['delay'],
    data(){
        return{
            showBlock: false,
            timer: null,
            reactionTime: 0,
        }
    },

    mounted(){
        setTimeout(() => {
            this.showBlock = true
            this.startTimer()
        }, this.delay)
    },

    methods:{
        startTimer(){
            this.timer = setInterval(() => {
                this.reactionTime += 10
            }, 10)
        },

        stopTimer(){
            clearInterval(this.timer),
            this.showBlock = false,
            this.$emit('reactionTime', this.reactionTime)
        }
    }
}
</script>

<style scoped>
    .block{
        width: 400px;
        border-radius: 20px;
        background-color: teal;
        color: white;
        text-align: center;
        padding: 100px;
        margin: 40px auto;
        
    }
</style>