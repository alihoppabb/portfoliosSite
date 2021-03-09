<template>
    <div class="box1">
        <router-link class="tx" to="/"><a class="nav-link active" aria-current="page" href="#">О нас</a></router-link>
        <router-link class="tx" to="/"><a  class="nav-link active" aria-current="page" href="#">Что</a></router-link>
    </div>
</template>

<script>
    export default {
        name: "navbar"
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
        color: burlywood;
        transition: 0.5s;
    }
    .tx a:hover{
        color: antiquewhite;
        transform: scale(1.3);
        transition: 0.5s;

    }
</style>