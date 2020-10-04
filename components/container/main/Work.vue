<template>
  <section id='work' class='h-auto md:h-screen bg-pink-100'>
    <div class='pt-12 md:pt-24'>
      <div class='pb-8'>
        <h1 class='ml-4 md:ml-12 text-5xl md:text-6xl text-gray-700 font-mono'>WORK</h1>
      </div>
      <!-- 将来的に公開するものが増えたらv-forで回す -->
      <div class='md:flex md:mx-4 my-4 py-2 md:border-2 md:border-black md:rounded'>
        <div class='w-screen md:w-1/2'>
          <img src='~/assets/image/work.png' data-src='~/assets/image/work.png' alt='brandmemoのホーム画像' class='workImage hidden md:block md:ml-4'>
          <img src='~/assets/image/work.png' data-src='~/assets/image/work.png' alt='brandmemoのホーム画像' class='smwork md:hidden'>
        </div>
        <div class='w-screen lg:w-1/2'>
          <a :href='this.url' target='_blank'>
            <button class='title font-semibold py-2 px-4 rounded'>
              <p class='text-lg md:text-3xl text-gray-700'>{{ this.title }}</p>
            </button>
          </a>
          <p class='text-sm md:text-lg mt-4 mr-4 text-gray-700'>{{ this.content }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
<script lang='ts'>
import { Vue, Component } from 'vue-property-decorator';
import 'lazysizes'
@Component
export default class Work extends Vue {
  readonly title = 'BRAND MEMO'
  readonly content = '株式投資の銘柄を選ぶために企業の分析やチャートの状態についてメモできるように作ったウェブサイトです。'
  readonly url = 'https://horizontal-ward-253909.web.app/'
}
</script>
<style scoped>
.workImage, .lazyloading {
  width: 600px;
  height: auto;
}
.smwork, .lazyloading {
  width: 300px;
  height: auto;
}
.title {
  transition: all 1s 0s ease;
}
.title:hover {
  background: #ccc;
}
</style>