<template>
<div class="firstvertical">
<section id ="overlay" class="overlay">
  <h1>Это невероятно, но мы сделаем все очень круто</h1>
  <section class="content overlay">
    <div class="firstvertical__text">
      <p>много текста или чего-то еще прям много очень что жопа ггорит как много я хуеваю
        много текста или чего-то еще прям много очень что жопа ггорит как много я хуеваю
        много текста или чего-то еще прям много очень что жопа ггорит как много я хуеваю
        много текста или чего-то еще прям много очень что жопа ггорит как много я хуеваю
        много текста или чего-то еще прям много очень что жопа ггорит как много я хуеваю
        много текста или чего-то еще прям много очень что жопа ггорит как много я хуеваю
        много текста или чего-то еще прям много очень что жопа ггорит как много я хуеваю
        много текста или чего-то еще прям много очень что жопа ггорит как много я хуеваю
        много текста или чего-то еще прям много очень что жопа ггорит как много я хуеваю
        много текста или чего-то еще прям много очень что жопа ггорит как много я хуеваю
        много текста или чего-то еще прям много очень что жопа ггорит как много я хуеваю
        много текста или чего-то еще прям много очень что жопа ггорит как много я хуеваю
        много текста или чего-то еще прям много очень что жопа ггорит как много я хуеваю
      </p>
    </div>
    <div class="firstvertical__image">
      <h1>This is image</h1>
    </div>
  </section>
</section>
</div>
</template>

<script>
import { gsap } from 'gsap'
import { Linear } from 'gsap'
export default {
name: "firstvertical",
  mounted() {
    const overlay = document.getElementById("overlay");
    let tl = new gsap.timeline({paused: true})
    tl.to(overlay,{duration: 2, autoAlpha: 0, y:'40vh', ease: Linear.easeNone})

    window.addEventListener("scroll", () => {
      const st = document.documentElement.scrollTop;
      const ht = overlay.scrollHeight;
      const windowScroll = st / ht;
      tl.progress(windowScroll);
    });
  }
}
</script>

<style>
.firstvertical {
  background: #071021;
}

.overlay {
  height: 100vh;
  background: pink;
  box-shadow: 0 100px 100px 100px pink;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: monospace;
  color: black;
  padding: 3em;
  text-align: center;
}

.content {
  font-family: monospace;
  color: #fff;
  padding: 2em;
  transform: translate3d(0, 0, 0);
  min-height: 100vh;
}

</style>