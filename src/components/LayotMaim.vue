<template>
<div class="container">
    <div class="row" > 
        <div  class="alert alert-danger" role="alert" >
           {{password}}
        </div>
    </div>

        <div class="row" > 
        <ul id="example-1">
             <li v-for="item in man" :key="item">
                     <div role="alert" :class="{'alert alert-primary':pr }" >
                        {{item}}
                    </div>
            </li>
        </ul>

  
    </div>
    <div class="row">
         <div class="mb-3 row">
            <label for="inputPassword" class="col-sm-2 col-form-label">Password</label>
            <div class="col-sm-10">
                <input type="text" class="form-control" id="inputPassword" v-model="password">
            </div>
        </div>   
        <a v-bind:href="link" > yandex </a>
        <div class="col-4">
             <button type="button" v-bind:disabled="isButtonDisabled"   class="btn btn-primary" v-on:click="dbutton">{{vbutton}}</button>
        </div>
    </div>
</div>
</template>

<script>
export default{
    name: 'LayotMaim',

    data(){
        return {
            password: "Мой пароль",
            color: "alert alert-danger",
            isButtonDisabled: false,
            link : "https://yandex.ru",
            vbutton: "Yandex",
            man: ["Маша ", "Даша", "Юля", "Света"],
            pr: true,
            tr: false
    }

    } ,
    methods:{
        check(){
            console.log("jjjj");
        },
        dbutton(){
            this.link = "https://rambler.ru";
            this.vbutton = "Rambler";
            this.isButtonDisabled = true;
            this.man.push(this.password);
            this.pr =false;

        }
    }
}

</script>