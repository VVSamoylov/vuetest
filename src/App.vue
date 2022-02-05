<template>
  <div class="container">
    <NavBar/>
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <MyModal/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import NavBar from  "@/components/NavBar";

 //eslint-disable-next-line
export default {
  name: "App",
  components: {
    HelloWorld,
    NavBar,
    
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
</style>
