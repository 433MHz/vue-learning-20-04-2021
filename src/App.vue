<template>
  <div id="contentDiv">
    <h1>Main component h1 tag</h1>
    <First :title="firstTitle" :theme="firstTheme"></First>
    <Second :title="secondTitle"></Second><br>

    <button @click="firstTheme = true">Make first red</button>
    <button @click="firstTheme = false">Make first blue</button>
  </div>
</template>


<script>
import First from './components/First.vue'
import Second from './components/Second.vue'
export default {
  components: { Second, First },
  
  data(){
    return{
      firstTitle: 'First title with binded data',
      secondTitle: 'Second title with binded data',

      firstTheme : false
    }
  }
}

</script>



<style scoped>
#contentDiv{
  width: 100%;
  height: 500px;
  background-color: lightgrey;
  margin: none;
  text-align: center;
}

</style>