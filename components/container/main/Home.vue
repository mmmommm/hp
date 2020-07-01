<template>
  <section id="home" class="md:h-screen md:flex md:items-center">
    <div class="md:w-1/2">
      <div class="hidden md:block flex md:ml-48 md:mt-16">
        <img src="~/assets/image/Bicycle1.JPG" alt="鹿児島で撮った自転車二台の映った画像" class="h-1/2 homeImage1">
        <img src="~/assets/image/Bicycle2.jpeg" alt="父母ヶ浜で撮った自転車と一緒に撮った画像" class="h-1/2 homeImage2">
      </div>
      <div class="md:hidden">
        <img src="~assets/image/homeImage.jpeg" alt="父母ヶ浜で撮った自転車と一緒に撮った画像">
      </div>
    </div>
    <div class="md:1/2 hidden md:block">
      <p class="md:text-6xl md:ml-48 text-center welcome">Welcome</p>
      <p class="md:text-6xl md:ml-48 text-center to">to</p>
      <!-- <p class="md:text-6xl text-center title">KISSE PORTFOLIO</p> -->
      <div class="flex flex-no-wrap md:ml-32 md:pb-24">
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
    var tl = gsap.timeline({ repeat: -1, repeatDelay: 0 })
      tl.from('.homeImage1', { duration: 2, delay: 1.5, opacity: 0 })
      tl.to('.homeImage1', { duration: 2, delay: 1, opacity: 0 })
      tl.from('.homeImage2', { duration: 2, delay: 0, opacity: 0 })
      tl.to('.homeImage2', { duration: 2, delay: 0.5, opacity: 0 })
    // gsap.from('.smImage', { duration: 2, delay: 5, opacity: 0 })
    gsap.fromTo('.welcome', { duration: 0.5, opacity: 0, y: 50 },{ delay: 1, opacity: 1, y: 150 })
    gsap.fromTo('.to', { duration: 0.5, opacity: 0, y: 300 }, { delay: 1.25,opacity: 1, y: 200 })
    gsap.to('.welcome', { duration: 0.5, delay: 2 , opacity: 0, y: 50})
    gsap.to('.to', { duration: 0.5, delay: 2.25 , opacity: 0, y: 250})
    document.querySelectorAll(".title").forEach((title, i) => {
      gsap.from(title, { duration:0.4, delay: 2.25 + i * 0.1, ease: 'power1.out', x: 50, y: -50, opacity: 0 })
    })
  }
}
</script>
<style scoped>
</style>