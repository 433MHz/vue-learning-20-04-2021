<template>
  <div id="contentDiv">
    <h1>Main component h1 tag</h1>
    <First title="First h1 tag from props"></First>
    <Second title="Second h1 tag from props"></Second>
  </div>
</template>


<script>
import First from './components/First.vue'
import Second from './components/Second.vue'
export default {
  components: { Second, First },
  
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