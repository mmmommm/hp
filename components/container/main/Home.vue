<template>
  <section id="home" class="md:h-screen md:flex md:justify-center md:items-center">
    <div class="hidden md:block">
      <img src="~/assets/image/bicycle.jpeg" alt="" class="homeImage">
    </div>
    <div class="md:hidden">
      <img src="~assets/image/homeImage.jpeg" alt="" class="smImage">
    </div>
    <div class="container justify-center">
      <p class="md:text-6xl text-center welcome">Welcome</p>
      <p class="md:text-6xl text-center to">to</p>
      <!-- <p class="md:text-6xl text-center title">KISSE PORTFOLIO</p> -->
      <div class="flex flex-no-wrap md:ml-48 md:pb-24">
        <div v-for="(text, i) in texts" :key="i">
          <p class="text-xl md:text-4xl title ml-2">{{ text }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
import { gsap } from 'gsap'
@Component
export default class Home extends Vue {
  texts: string[] = [
    "K","I","S","S","E"," ", " ","P","O","R","T","F","O","R","I","O"
  ]
  mounted() {
    gsap.from('.homeImage', { duration: 2, delay: 1, opacity: 0 })
    gsap.from('.smImage', { duration: 2, delay: 5, opacity: 0 })
    gsap.from('.welcome', { duration: 0.5, delay: 1, opacity: 0, y: 50 })
    gsap.from('.to', { duration: 0.5, delay: 1.25 , opacity: 0, y: -50 })
    gsap.to('.welcome', { duration: 0.5, delay: 1.75 , opacity: 0, y: 50})
    gsap.to('.to', { duration: 0.5, delay: 2 , opacity: 0, y: -50})
    // gsap.fromTo('.title', { duration: 0.5, delay: 2.25 ,opacity: 0 }, { duration: 0.5, delay:2.25 ,opacity: 1, y:-100})
    document.querySelectorAll(".title").forEach((title, i) => {
      gsap.from(title, { duration:0.4, delay: 2 + i * 0.1, ease: 'power1.out', x: 50, y: -50, opacity: 0 })
    })
  }
}
</script>
<style scoped>
.homeImage {
  width: 100%;
  height: auto;
}
</style>