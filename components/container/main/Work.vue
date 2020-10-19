<template>
  <section id='work' class='h-auto bg-pink-100'>
    <div class='pt-12 md:pt-24'>
      <div class='pb-8'>
        <h1 class='ml-4 md:ml-12 text-5xl md:text-6xl text-gray-700 font-mono'>WORK</h1>
      </div>
      <div
        v-for='(work, i) in works'
        :key='work.id'
        :data-index='i'
      >
        <div class='md:flex md:mx-4 my-4 py-2 md:border-2 md:border-black md:rounded'>
          <div class='w-screen md:w-1/2'>
            <img :src="require('~/static/work/' + work.src)" :data-src="require('~/static/work/' + work.src)" alt='作品のホーム画像' class='workwork hidden md:block md:ml-4'>
            <img :src="require('~/static/work/' + work.src)" :data-src="require('~/static/work/' + work.src)" alt='作品のホーム画像' class='smwork md:hidden'>
          </div>
          <div class='w-screen lg:w-1/2 ml-4 md:ml-8'>
            <a :href='work.url' target='_blank' rel='noopener'>
              <button class='title font-semibold py-2 px-4 rounded' name='work-link'>
                <p class='text-lg md:text-3xl text-gray-700'>{{ work.title }}</p>
              </button>
            </a>
            <p class='text-sm md:text-lg mt-4 mr-4 text-gray-700'>{{ work.content }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script lang='ts'>
import { Vue, Component } from 'vue-property-decorator';
import { workCard } from '@/interface/workCard';
import 'lazysizes'
@Component
export default class Work extends Vue {
  works: workCard[] = [
    {
      id: 1,
      src: 'brandmemo.png',
      title: 'BRAND MEMO',
      content: '株式投資の銘柄を選ぶために企業の分析やチャートの状態についてメモできるように作ったウェブサイトです。',
      url: 'https://horizontal-ward-253909.web.app/'
    },
    {
      id: 2,
      src: 'portfolio.png',
      title: 'KISSE PORTFOLIO',
      content: 'このサイトです、パフォーマンスに気を使い、色合いも目に優しいものを目指しました。',
      url: 'https://github.com/mmmommm/kisse-portfolio'
    },
    {
      id: 3,
      src: 'tenki.png',
      title: 'tenki',
      content: 'Golangで作成したCLIツールです、天気予報と現在の気象情報を確認できます。',
      url: 'https://github.com/mmmommm/tenki'
    },
  ]
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