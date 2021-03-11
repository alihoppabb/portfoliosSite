<template>
<div class="panel__two">
  <div id="trigger" class="spacer s0"></div>
  <div id="reveal1" class="slide">

    <div class="sl1">
      <img src="../assets/medium.png" alt="" class="panel__img">
      <h1 class="panel__text">asdfds</h1>
    </div>
    <div class="sl2">
      <img src="../assets/medium.png" alt="" class="panel__img">
      <h1 class="panel__text">ASDF</h1>
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
    let tl2 = new gsap.timeline()
    tl.from(".sl1", {duration: 1, y: -1000})
    tl2.from(".sl2", {duration: 1, y: 1000})
    new ScrollMagic.Scene({triggerElement: "#trigger", triggerHook: "0.4"})
        .setTween(tl)
        .setClassToggle("#reveal1", "visible")
        .addIndicators() // add indicators (requires plugin)
        .addTo(controller);
    new ScrollMagic.Scene({triggerElement: "#trigger", triggerHook: "0.4"})
        .setTween(tl2)
        .setClassToggle("#reveal1", "visible")
        .addIndicators() // add indicators (requires plugin)
        .addTo(controller);
  }
}
</script>

<style scoped>

.panel__two {
}

.slide{
  display: flex;
  justify-content: space-around;
  margin-top: 10%;
}

#trigger {
  overflow: hidden;
}

.sl1{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.sl2{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
#reveal1{
  opacity: 0;
}
#reveal1.visible{
  opacity: 1;
}
.panel__img{
  height: 40%;
  width: 40%;
}

.panel__img:nth-child(1) {
}

.panel__text {
  top: 0;
  text-align: center;
}

</style>