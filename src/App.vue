<template>
<!-- 
<button @click="setselectedTab('comp-comp1')" type="button" class="btn btn-primary">Registration Form</button>
<button @click="setselectedTab('comp-comp2')" type="button" class="btn btn-success">Frequently asked Questions</button>
<button @click="setselectedTab('comp-comp3')" type="button" class="btn btn-danger">MORNING</button>
<button @click="setselectedTab('comp-comp4')" type="button" class="btn btn-warning">EVENING</button> -->
<main-comp></main-comp>



 <component :is="selectedTab"></component>
</template>

<script>

import CompComp1 from './components/CompComp1.vue'
import CompComp2 from './components/CompComp2.vue'
import CompComp3 from './components/CompComp3.vue'
import CompComp4 from './components/CompComp4.vue'
import MainComp from './components/MainComp.vue'



export default {
  name: 'App',
  components: {

    CompComp1,
    CompComp2,
    CompComp3,
    CompComp4,
    MainComp
 

    
 
  },
  data(){
    return {
      selectedTab: '',	
  }
},
methods:{
  setselectedTab(tab){
    this.selectedTab = tab
  }
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
  
  
}
button{
  margin: 1rem;
  
}
</style>
