<template>
  <div class="home">
    <div id="pinMaster">
      <div id="pinContainer">
        <section class="panel one">
          <h1>Pin Panel A</h1>
        </section>
        <section class="panel two">
          <h1>Pin Panel B</h1>
        </section>
        <section class="panel three">
          <h1>Pin Panel C</h1>
        </section>
        <section class="panel four">
          <h1>Pin Panel D</h1>
        </section>
        <section class="panel five">
          <h1>Pin Panel E</h1>
        </section>
        <section class="panel six">
          <h1>Pin Panel F</h1>
        </section>
      </div>

    </div>
  </div>
  <div>
    <nav>
      <ul>
        <li>rot</li>
        <li>git</li>
        <li>ebal</li>
      </ul>
      <ul>
        <li></li>
        <li></li>
        <li></li>
      </ul>
      <ul>
        <li></li>
        <li></li>
        <li></li>
      </ul>
    </nav>
  </div>
</template>

<script>
  import AOS from 'aos';
  import 'aos/dist/aos.css';
  import  { gsap } from "gsap"
  import { Linear } from 'gsap'
  import * as ScrollMagic from "scrollmagic"; // Or use scrollmagic-with-ssr to avoid server rendering problems
  import { TweenMax, TimelineMax } from "gsap"; // Also works with TweenLite and TimelineLite
  import { ScrollMagicPluginGsap } from "scrollmagic-plugin-gsap";

  ScrollMagicPluginGsap(ScrollMagic, TweenMax, TimelineMax);

  export default {
    name: 'Home',
    components: {
    },
    mounted() {
      AOS.init();
      console.clear();
      let controller = new ScrollMagic.Controller();
      let sections = document.querySelectorAll("section");
      let tl = new gsap.timeline
      for (let i = 1; i < sections.length; i++) {
        tl.from(sections[i], {duration: 1,  xPercent:100, ease: Linear.easeNone }, "+=1");
      }

      new ScrollMagic.Scene({
        triggerElement: "#pinMaster",
        triggerHook: "onLeave",
        duration: "500%"
      })
              .setPin("#pinMaster")
              .setTween(tl)
              .addIndicators({
                colorTrigger: "white",
                colorStart: "white",
                colorEnd: "white",
                indent: 40
              })
              .addTo(controller);

    }
  }
</script>
<style>
  body,
  html {
    height: 100%;
    font-size: 16px;
    font-weight: normal;
    font-family: "Roboto", sans-serif;
    color: white;
    background-color: #f0f0ee;
    margin: 0px;
    padding: 0;
  }

  h1 {
    font-size: 32px;
    color: white;
    position: relative;
    display: block;
    top: 40%;
    text-align: center;
    text-transform: uppercase;
  }

  #pinContainer {
    width: 100%;
    height: 100vh;
    overflow: hidden;
    position: relative;
  }
  .panel {
    height: 100%;
    width: 100%;
    position: absolute;
  }

  #pinMaster {
    position: relative;
  }

  .one {
    background-color: #1bb1a5;
  }
  .two {
    background-color: #94c356;
  }
  .three {
    background-color: #e3aa59;
  }
  .four {
    background-color: #777;
  }

  .five {
    background-color: #a63ba0;
  }
  .six {
    background-color: #cf5b21;
  }
</style>