<template>
 
  <NavBar/>
  
  <trafficLights title="Привет!"/>
  
</template>

<script>
import NavBar from '@/components/NavBar';
import trafficLights from '@/components/trafficLights';

export default {
  name: 'App',
  components: {
    NavBar,
    trafficLights
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
