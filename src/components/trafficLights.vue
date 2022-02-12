<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class = "col-2 lith">

                   <h1> {{title}} </h1>
                   <fonar color="red.jpg" />
                   <fonar color="yellow.jpg" />
                   <fonar color="green.jpg" />
                  <button type="button" class="btn btn-info" @click="chenge">Переключить</button>
            </div>
          
        </div>
       
    </div>
</template>

<script>
import fonar from '@/components/fonar';
export default {
    name: 'trafficLights',
    components: {
        fonar
    },
    props:['title'],
    data(){
        return{
            first: 'red',
            lights :{
                red: true,
                yellow: false,
                green: false,
            }
        }
    },
    methods:{
            chenge(){
                if(this.lights.red){
                    this.lights.red = false;
                    this.lights.yellow = true;
                }
                if(this.lights.yellow){
                    this.lights.yellow = false;
                    this.lights.green = true;
                }
                if(this.lights.green){
                    this.lights.green = false;
                    this.lights.red =true;
                }

                console.log("press");
                console.table(this.lights);
            }
    }
}
</script>

<style>
.lith{
    border-style: solid;
    border-color: black;
    border-width: 4 px;
    width: 400 px;
}
 
</style>