<template>
    <div class="col-2 " @click="test">
        
        <img v-bind:src="colorCurrent" class="rounded-circle fon" alt="...">
    </div>    
</template>

<script>
export default {
    name: 'fonar',
    props:{
        color:String
    },
    data(){
        return{
            colorZ: false,
            colorCurrent: ""
        }
    }, 
    methods:{
        test(){
            console.log(this.colorZ)
            console.log(this.colorCurrent)
            if(this.colorZ){
                this.$data.colorCurrent =  require("../assets/white.jpg");
                this.colorZ = false;
            }else{ 
                this.$data.colorCurrent =  require(`../assets/${this.$props.color}`);
                this.colorZ= true;
           }
        }
    }
};

</script>

<style>
.rounded-circle{
    border-style: solid;
    border-color: black;
    border-width: 1px;
    width: 150px;
    margin-top: 5px;
}

</style>
