<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class = "col-2 lith">

                   <h1> {{title}} </h1>
                   <fonar :color="lights.red" />
                   <fonar :color="lights.yellow" />
                   <fonar :color="lights.green" />
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
            lights :{
                red: 'white',
                yellow: 'yellow',
                green: 'white',
            }
        }
    },
    methods:{
            chenge(){
                if(this.lights.red == 'red'){
                    this.lights.red = 'white';
                    this.lights.yellow = 'yellow';
                }else if (this.lights.yellow == 'yellow'){
                    this.lights.yellow = 'white';
                    this.lights.green = 'green';
                }else if(this.lights.green == 'green'){
                    this.lights.green = 'white';
                    this.lights.red = 'red';
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
    margin-top: 25px;
    width: 400 px;
    height: 700px;
}
 button{
     margin-top: 25px;
 }
</style>