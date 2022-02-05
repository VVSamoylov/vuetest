<template>
  <div class="row justify-content-center">
    <div class="col-4 proj">
      <fonar color="red.jpg"/>
      <fonar color="green.jpg"/>
      <fonar color="yellow.jpg"/>
    </div>
  </div>
</template>

<script>
import fonar from '@/components/fonar.vue';
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  components:{
    fonar
  },
};
</script>


<style scoped>
.proj {
  margin-top: 50px;
  padding-top:10px ;
  border-width: 5px;
  border-color: black;
  border-style: solid;
  width: 200px;
  height: 400px;
}

</style>
