<template>
    <div>
        <input type="date" v-model="data">
        <data-comp :dataParam="data"> </data-comp>
    </div>
    
</template>

<script>
import DataComp from './components/dataComp.vue'

export default {
  data(){
    return{
      data: null
    }
  },

  components: {
    DataComp
  },

  computed: {

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
