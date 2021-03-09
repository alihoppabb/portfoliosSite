<template>
    <div class="firsPanel">
        <div class="sections" id="js-slideContainer">
            <section class="section">
                <div class="sectionTitle" id="title1">
                    <div class="image">
                        <img src="../assets/small.png" alt="">
                        <img src="../assets/medium.png" alt="">
                        <img src="../assets/large.png" alt="">
                    </div>
                </div>
            </section>
        </div>
    </div>
</template>

<style scoped>
    .image img:nth-child(1) {
        width: 100px;
        height: 100px;
        position: absolute;
        right: 170px;
        top: 340px;
    }
    .image img:nth-child(2) {
        width: 120px;
        height: 200px;
        position: absolute;
        right: 170px;
        top: 330px;
    }

    .image img:nth-child(3) {
        width: 500px;
        height: 500px;
        position: absolute;
        right: 100px;
        top: 180px;
        z-index: 3;
    }

</style>

<script>
    import { gsap } from "gsap"
    import { Linear } from 'gsap'
    import { TweenLite } from 'gsap'
    export default {
        name: "firstPanel",
        mounted() {
            TweenLite.defaultEase = Linear.easeNone;
            let image = document.querySelectorAll(".image img");
            let tl = new gsap.timeline({default: {duration: 1}});

// create timeline
// this could also be created in a loop
            tl.from(image[2], {duration: 0.5, scale: 4, opacity: 0})
// tl.from(image[1], {opacity: 0})
// tl.from(image[0], {opacity: 0})
            tl.to(image[1], {duration: 1, y: -155, x: -280})
            tl.to(image[0], {duration: 1, y: -165, x: -420})


        }
    }
</script>