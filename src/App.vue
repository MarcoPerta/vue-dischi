<template>
  <div id="app">
    <HeaderComp/>

    <MainComp @emitGeneri="methodEmitApp" :emit="methodEmitApp"/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import MainComp from './components/MainComp.vue'


export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp
  },
  data() {
        return {
            arrayGeneri: []
        }
    },
  methods:{
    methodEmitApp(valoreEmit){
      this.arrayGeneri=valoreEmit;
    }
  }  
  
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100vw;
  height: 100vh;
}
</style>
