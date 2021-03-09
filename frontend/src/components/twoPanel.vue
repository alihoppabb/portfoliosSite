<template>
<div>
  <div id="reveal1" class="slide">
    <div id="trigger" class="spacer s0"></div>
    <div class="sl1">
      <img src="../assets/medium.png" alt="">
      <h1>asdfds</h1>
    </div>
    <div class="sl2">
      <img src="../assets/medium.png" alt="">
      <h1>ASDF</h1>
    </div>
  </div>
</div>
</template>

<script>
import { gsap } from "gsap"
import * as ScrollMagic from "scrollmagic";
export default {
name: "twoPanel",
  mounted() {
    var controller = new ScrollMagic.Controller({vertical: false,default: {duration: 1}});
    let tl = new gsap.timeline();
    tl.from(".sl1", {duration: 1, x: 1000})
    tl.from(".sl2", {duration: 1, x: 1000})
    new ScrollMagic.Scene({triggerElement: "#trigger", triggerHook: "0.4"})
        .setTween(tl)
        .setClassToggle("#reveal1", "visible")
        .addIndicators() // add indicators (requires plugin)
        .addTo(controller);
  }
}
</script>

<style scoped>
.slide{
  display: flex;
  flex-wrap: nowrap;
  flex-direction: row;

}
.sl1{
  margin-left: 25%;
  margin-top: 15%;
}
.sl2{
  margin-left: 35%;
  margin-top: 15%;
}
#reveal1{
  opacity: 0;
}
#reveal1.visible{
  opacity: 1;
}
img{
  height: 250px;
  width: 250px;
}
</style>