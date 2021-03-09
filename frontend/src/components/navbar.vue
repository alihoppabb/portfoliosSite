<template>
    <div class="box1">
        <router-link class="tx" to="/"><a id="one" class="nav-link active" aria-current="page" href="#">Здесь наше название</a></router-link>
        <router-link class="tx" to="/"><a id="two"  class="nav-link active" aria-current="page" href="#">Что</a></router-link>
    </div>
</template>

<script>
import gsap from 'gsap'
import { Linear } from 'gsap'
import { TextPlugin } from "gsap/TextPlugin";
gsap.registerPlugin(TextPlugin);
    export default {
        name: "navbar",
      mounted() {
        let text = document.getElementById("one");
        let tl = new gsap.timeline({repeat:-1, yoyo:false, repeatDelay:0, onCompleteParams:["test1", "test2"]});

        tl.to(text, 0.8, {text:{value:"Здесь наше < html >", padSpace:true,  ease:Linear.easeNone},delay:2});
        tl.to(text, 0.8, {text:{value:"Сайты под ключ", padSpace:true, ease:Linear.easeNone},delay:2});
        tl.to(text, 0.8, {text:{value:"Высокий уровень работы", padSpace:true, ease:Linear.easeNone},delay:2});

        let text2 = document.getElementById("two");
        let tl2 = new gsap.timeline({repeat:-1, yoyo:false, repeatDelay:0, onCompleteParams:["test1", "test2"]});

        tl2.to(text2, 0.8, {text:{value:"Чт№", padSpace:true,  ease:Linear.easeNone},delay:2});
        tl2.to(text2, 0.8, {text:{value:"Ч№#", padSpace:true, ease:Linear.easeNone},delay:2});
        tl2.to(text2, 0.8, {text:{value:"@то", padSpace:true, ease:Linear.easeNone},delay:2});
        tl2.to(text2, 0.8, {text:{value:"@т#", padSpace:true, ease:Linear.easeNone},delay:2});
      }
    }
</script>

<style scoped>
    .box1{

        margin-top: 35px;
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;
        justify-content: space-between;
        z-index: 2;
    }
    .tx{
        font-size: 35px;
        text-decoration: none;
        margin-left: 150px;
        margin-right: 150px;
    }
    .tx a{
        color: #ce33eb;
        transition: 0.5s;
        text-shadow: 2px 4px 3px rgba(0,0,0,0.3);
        font-family: Impact;

    }
    .tx a:hover{
        color: #7275a3;
        transform: scale(1.3);
        transition: 0.5s;
        text-shadow: 2px 4px 3px rgba(0,0,0,0.3);


    }
</style>