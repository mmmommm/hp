<template>
  <section id='home' class='md:h-screen md:flex md:items-center bg-pink-100'>
    <div class='md:w-1/2'>
      <div class='hidden md:block flex md:ml-48 md:mt-32 lg:mt-12'>
        <img src='~/assets/image/Bicycle1.JPG' alt='鹿児島で撮った自転車二台の映った画像' class='h-1/2 homeImage1 object-scale-down'>
        <img src='~/assets/image/Bicycle2.jpeg' alt='父母ヶ浜で撮った自転車と一緒に撮った画像' class='h-1/2 homeImage2'>
      </div>
      <div class='md:hidden'>
        <img src='~assets/image/smhome.jpeg' data-src='~assets/image/smhome.jpeg' alt='父母ヶ浜で撮った自転車と一緒に撮った画像' class='smimage'>
      </div>
    </div>
    <div class='md:w-1/2'>
      <p class='md:text-6xl md:ml-32 text-center welcome hidden md:block text-gray-700'>Welcome</p>
      <p class='md:text-6xl md:ml-32 text-center to hidden md:block text-gray-700'>to</p>
      <div class='flex flex-no-wrap -mt-16 md:mt-0 pl-4 md:ml-48 md:pb-24 text-pink-100 md:text-gray-700'>
        <div v-for='(text, i) in texts' :key='i'>
          <p class='text-xl md:text-4xl title ml-2'>{{ text }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
<script lang='ts'>
import { Vue, Component } from 'vue-property-decorator';
import { gsap } from 'gsap'
@Component
export default class Home extends Vue {
  readonly texts: string[] = [
    'K','I','S','S','E',' ', ' ','P','O','R','T','F','O','R','I','O'
  ]
  mounted() {
    var tl = gsap.timeline({ repeat: -1, repeatDelay: 0 })
      tl.from('.homeImage1', { duration: 2, delay: 1.5, opacity: 0 })
      tl.to('.homeImage1', { duration: 2, delay: 1, opacity: 0 })
      tl.from('.homeImage2', { duration: 2, delay: 0, opacity: 0 })
      tl.to('.homeImage2', { duration: 2, delay: 0.5, opacity: 0 })
    gsap.fromTo('.welcome', { duration: 0.5, opacity: 0, y: 50 },{ delay: 1, opacity: 1, y: 150 })
    gsap.fromTo('.to', { duration: 0.5, opacity: 0, y: 300 }, { delay: 1.25,opacity: 1, y: 200 })
    gsap.to('.welcome', { duration: 0.5, delay: 2 , opacity: 0, y: 50})
    gsap.to('.to', { duration: 0.5, delay: 2.25 , opacity: 0, y: 250})
    document.querySelectorAll('.title').forEach((title, i) => {
      gsap.from(title, { duration:0.4, delay: 2.25 + i * 0.1, ease: 'power1.out', x: 50, y: -50, opacity: 0 })
    })
  }
}
</script>
<style scoped>
.homeImage1, .homeImage2, .lazyloading {
  height: 400px;
  width: 600px;
}
.smimage, .lazyloading {
  height: 700px;
  width: 100%;
}
</style>