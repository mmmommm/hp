<template>
  <div class='pt-24 md:pt-16 bg-pink-100 border-b'>
    <div>
      <h1 class='text-3xl md:text-5xl text-gray-700 ml-16 md:ml-24 font-mono'>SKILLS</h1>
    </div>
    <div class='flex flex-wrap mt-4 md:mt-8 px-4 md:px-40'>
      <div
        v-for='(skillDetail, i) in skillDetails'
        :key='skillDetail.id'
        :data-index='i'
        class='w-screen md:w-1/2 py-4 my-2'
      >
        <div>
          <div class='flex skillTitle'>
            <img :src="require('~/assets/icon/' + skillDetail.src)" alt='それぞれの技術のアイコン' class='w-1/2 icon'/>
            <p class='text-base md:text-2xl ml-1 md:ml-4 text-gray-700 my-auto w-1/2'>{{ skillDetail.name }}</p>
          </div>
          <div class='skill-talk'>
            <p class='text-gray-700'>期間：{{ skillDetail.period }}</p>
            <p class='text-gray-700 mx-4'>{{ skillDetail.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script lang='ts'>
import { Vue, Component } from 'vue-property-decorator';
import { skillDetail } from '~/interface/skillDetail';
import { gsap } from 'gsap'
@Component
export default class SkillDetail extends Vue {
  skillDetails: skillDetail[] = [
    {
      id: 1,
      name: 'HTML',
      src: 'html.png',
      period: '一年ちょっと',
      description: 'プログラミングを学び始めたときに最初に触ったマークアップ言語です。特にいうことないです。'
    },
    {
      id: 2,
      name: 'CSS',
      src: 'css.png',
      period: '一年ちょっと',
      description: 'HTMLと同じ時期に触り始めました、先日あったインターンで理解の浅さが出てしまったのでしっかり学びます。'
    },
    {
      id: 3,
      name: 'Typescript',
      src: 'ts.png',
      period: '半年ぐらい',
      description: 'vueとかのフレームワークを使用するときに使っているので、js自体にとても詳しいってわけじゃないところ直したいです、最近は全てtsで書くようにしているので少しは使えるようになっていると思います。'
    },
    {
      id: 4,
      name: 'Vue/Nuxt',
      src: 'vue.png',
      period: '一年ぐらい',
      description: '最近自分で作成したアプリケーションをcomposition-apiに書き直しました。普通にかけます。'
    },
    {
      id: 5,
      name: 'React/Next',
      src: 'react.png',
      period: '一ヶ月ぐらい',
      description: '友人と作成しているウェブアプリのフロントエンド部分で使用しています、nextのアップデート情報をみてすごく今触りたいです。'
    },
    {
      id: 6,
      name: 'Git',
      src: 'github.png',
      period: '一年ちょっと',
      description: '基本的な機能は使えるつもりです、だいぶ慣れては来ましたがたまに怖い時があります。。。'
    },
    {
      id: 7,
      name: 'Docker',
      src: 'docker.png',
      period: '三ヶ月ぐらい',
      description: '開発環境整えるぐらいしかできないです、これもやらなきゃいけないとは思ってるんですけどね。。。'
    },
    {
      id: 8,
      name: 'CirclCI',
      src: 'circleci.png',
      period: '三ヶ月ぐらい',
      description: '自分で作ったウェブアプリを自動デプロイするのに使いました、書き方はわかります。'
    },
    {
      id: 9,
      name: 'Firebase',
      src: 'firebase.png',
      period: '一年ちょっと',
      description: 'ほとんどサーバーサイドの機能を任せています、大体の機能は使えるつもりですがfirestoreの設計はあまり自信がありません。'
    },
    {
      id: 10,
      name: 'Golang',
      src: 'go.png',
      period: '三ヶ月ぐらい',
      description: '最近触り始めました、slackbotとCLIツールを作りました、これからしっかりと学んでいきたいです。'
    },
    {
      id: 11,
      name: 'php/Laravel',
      src: 'php.png',
      period: '一ヶ月ぐらい',
      description: 'インターン先で使用しました、検索処理の改善を行いました。'
    }

  ]
  mounted() {
    document.querySelectorAll('.skillTitle').forEach((skillTitle, i) => {
      gsap.from(skillTitle, { duration:3, delay: i * 0.6, ease: 'bounce.out', y: 50, opacity: 0 })
    })

    gsap.from('.skill-talk', { duration:3, delay: 2.5, ease: 'back.out(1.7)', y: -100, opacity: 0})
  }
}
</script>
<style scoped>
.icon {
  width: 60px;
  height: 60px;
}
</style>