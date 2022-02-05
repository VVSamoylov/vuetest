<template>
  <div v-if="dsp" >
    <p> Имя {{fname}} </p>
    <p> Отчество {{lname}}</p>
    <button type="button" class="btn btn-primary" @click="changeName" > Изменить </button>
  </div>
  <br/>
  <div>
    <button type="button" class="btn btn-secondary" @click="stels" >{{dsp? "Спрятать" : "Показать"}}</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return {
      fname: 'Полиграф',
      lname: 'Полиграфович',
      dsp: true
    }
  },
  methods: {
    changeName(){
      this.fname = "Иван";
      this.lname = "Иваныч";
    },
    stels(){
        this.dsp = !this.dsp;
    } 
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
