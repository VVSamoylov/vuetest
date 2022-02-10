<template>
<div class="row">
    <div>
       {{color}}
       <img   v-bind:src="colorCurrent" class="rounded-circle" alt="..." @click="colorset">
    </div>
</div>
</template>
<script>
export default{
    name: 'fonar',
    props:{
        color : String,
        position: Number
    },
    data(){
        return{
            colorCurrent: '',
            currentPosition: '',
            colorZ: false
        }
    },
    methods:{
        colorset(){
            if(this.colorZ){
                this.colorCurrent = require('../assets/white.jpg');
                this.colorZ = false;
            }else{
                    this.colorCurrent = require(`../assets/${this.$props.color}.jpg`);
                    this.colorZ =  true;

            }
            
        }
    },
    mounted(){
        //this.colorCurrent = require('../assets/white.jpg');
        //this.curentPosition = this.props.position;
         this.colorCurrent = require(`../assets/${this.$props.color}.jpg`);
    },
    updated(){
         this.colorCurrent = require(`../assets/${this.$props.color}.jpg`);
    }
}
</script>
<style>
.rounded-circle{
    border-style: solid;
    border-color: black;
    border-width: 3 px;
    width: 150px;
    margin-top: 5px;
}
</style>