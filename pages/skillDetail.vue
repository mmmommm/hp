<template>
  <div class="pt-24 md:pt-16 bg-gray-900 border-b">
    <div>
      <h1 class="text-3xl md:text-5xl text-white ml-16 md:ml-24">SKILLS</h1>
    </div>
    <div class="flex flex-wrap mt-4 md:mt-8 px-4 md:px-40">
      <div
        v-for="(skillDetail, i) in skillDetails"
        :key="skillDetail.id"
        :data-index="i"
        class="w-full md:w-1/2 py-4 my-2"
      >
        <div>
          <div class="flex skillTitle">
            <img :src="require('~/static/skill/' + skillDetail.src)" alt="" class="w-1/2 icon"/>
            <p class="text-base md:text-2xl ml-1 md:ml-4 text-white my-auto w-1/2">{{ skillDetail.name }}</p>
          </div>
          <div class="skill-talk">
            <p class="text-white">期間：{{ skillDetail.period }}</p>
            <p class="text-white mx-4">{{ skillDetail.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
import { skillDetail } from "~/interface/skillDetail";
import { gsap } from 'gsap'
@Component
export default class SkillDetail extends Vue {
  skillDetails: skillDetail[] = [
    {
      id: 8,
      name: "HTML",
      src: "html.png",
      period: "一年ちょっと",
      description: "プログラミングを学び始めたときに最初に触ったマークアップ言語です。特にいうことないです。"
    },
    {
      id: 7,
      name: "CSS",
      src: "css.png",
      period: "一年ちょっと",
      description: "HTMLと同じ時期に触り始めました、vuetifyとかのUIフレームワークに逃げてしまっていたので、これから深く理解していきたいです。"
    },
    {
      id: 6,
      name: "Typescript",
      src: "ts.png",
      period: "半年ぐらい",
      description: "vueとかのフレームワークを使用するときに使っているので、js自体にとても詳しいってわけじゃないところ直したい。。。"
    },
    {
      id: 5,
      name: "Vue/Nuxt",
      src: "nuxt.png",
      period: "一年ぐらい",
      description: "基本的にフロントエンドはこれで書いています、大抵の処理はかけますがコンポーネントの分割とかが苦手なのをどうにかしたいです。"
    },
    {
      id: 4,
      name: "GitHub",
      src: "github.jpg",
      period: "一年ちょっと",
      description: "基本的な機能は使えるつもりですが、rebaseとかあんまり自信がないです、どっかでまとめてやりたいです。"
    },
    {
      id: 3,
      name: "Docker",
      src: "docker.png",
      period: "三ヶ月ぐらい",
      description: "開発環境整えるぐらいしかできないです、これもやらなきゃいけないとは思ってるんですけどね。。。"
    },
    {
      id: 2,
      name: "CirclCI",
      src: "circleci.png",
      period: "三ヶ月ぐらい",
      description: "自分で作ったウェブアプリを自動デプロイするのに使いました、書き方はわかります。"
    },
    {
      id: 1,
      name: "Firebase",
      src: "firebase.png",
      period: "一年ちょっと",
      description: "ほとんどサーバーサイドの機能を任せています、大体の機能は使えるつもりですがSQLの知識がなさすぎてfirestoreの設計ができません。。。"
    }
  ]
  mounted() {
    document.querySelectorAll(".skillTitle").forEach((skillTitle, i) => {
      gsap.from(skillTitle, { duration:3, delay: i * 0.6, ease: 'bounce.out', x: 50, opacity: 0 })
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