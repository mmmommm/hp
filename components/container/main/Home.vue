<template>
  <section id='home' class='md:h-screen md:flex md:items-center bg-pink-100'>
    <div class='md:w-1/2'>
      <div class='hidden md:block flex md:ml-48 md:mt-32 lg:mt-12'>
        <img src='~/assets/image/Bicycle1.JPG' alt='鹿児島で撮った自転車二台の映った画像' class='h-1/2 homeImage1 object-scale-down'>
        <img src='~/assets/image/Bicycle2.jpeg' alt='父母ヶ浜で撮った自転車と一緒に撮った画像' class='h-1/2 homeImage2'>
      </div>
      <div class='md:hidden'>
        <img src='~assets/image/smhome.jpeg' data-src='~assets/image/smsize.jpeg' alt='父母ヶ浜で撮った自転車と一緒に撮った画像' class='smimage'>
      </div>
    </div>
    <div class='md:w-1/2 text-center'>
      <p class='md:text-6xl welcome hidden md:block text-gray-700'>Welcome</p>
      <p class='md:text-6xl to hidden md:block text-gray-700'>to</p>
      <div class='flex flex-no-wrap -mt-16 md:mt-0 md:pb-24 text-pink-100 md:text-gray-700 ml-4 md:ml-0 md:justify-center'>
        <div v-for='(text, i) in texts' :key='i'>
          <p class='text-xl md:text-4xl title ml-1'>{{ text }}</p>
        </div>
      </div>
      <div class='hidden md:block'>
        <a class='btn_scroll ml-4 xl:ml-8' href='javascript:void(0)'>
        <span></span>
        scroll
        </a>
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
  height: 640px;
  width: 100%;
}
a.btn_scroll {
  position: absolute;
  bottom: -15px;
  left: 72%;
  z-index: 2px;
  display: inline-block;
  transform: translate(0, -50%);
  text-decoration: none;
  padding-top: 60px;
  color: #feb2b2;
}
a.btn_scroll span {
  position: absolute;
  top: 0;
  left: 72%;
  width: 30px;
  height: 50px;
  margin-left: -20px;
  border: 2px solid #feb2b2;
  border-radius: 50px;
  box-sizing: border-box;
}
a.btn_scroll span::before {
  position: absolute;
  top: 10px;
  left: 72%;
  content: '';
  width: 6px;
  height: 6px;
  margin-left: -9px;
  background-color: #feb2b2;
  border-radius: 100%;
  -webkit-animation: sdb 2s infinite;
  animation: sdb 2s infinite;
  box-sizing: border-box;
}
@keyframes sdb {
  100% {
    top: 30px;
    opacity: 0;
  }
}
</style>