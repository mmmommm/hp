<template>
  <div class="pt-24 md:pt-16 bg-gray-900 border-b">
    <div>
      <h1 class="text-3xl md:text-5xl text-white ml-16 md:ml-24">SKILLS</h1>
    </div>
    <div class="flex flex-wrap mt-4 md:mt-8 px-4 md:px-48">
      <div
        v-for="(skillDetail, i) in skillDetails"
        :key="skillDetail.id"
        :data-index="i"
        class="w-full md:w-1/2 py-4 my-2"
      >
        <div>
          <div class="flex">
            <img :src="require('~/static/skill/' + skillDetail.src)" alt="" class="w-1/2 icon"/>
            <p class="text-base md:text-2xl ml-1 md:ml-4 text-white my-auto w-1/2">{{ skillDetail.name }}</p>
          </div>
          <p class="text-white">期間：{{ skillDetail.period }}</p>
          <p class="text-white">{{ skillDetail.discription }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
import { skillDetail } from "~/interface/skillDetail";
export default class SkillDetail extends Vue {
  skillDetails: skillDetail[] = [
    {
      id: 8,
      name: "HTML",
      src: "html.png",
      period: "一年ちょっと",
      discription: "プログラミングを学び始めたときに最初に触った技術です"
    },
    {
      id: 7,
      name: "CSS",
      src: "css.png",
      period: "",
      discription: ""
    },
    {
      id: 6,
      name: "Typescript",
      src: "ts.png",
      period: "",
      discription: ""
    },
    {
      id: 5,
      name: "Vue/Nuxt",
      src: "nuxt.png",
      period: "",
      discription: ""
    },
    {
      id: 4,
      name: "GitHub",
      src: "github.jpg",
      period: "",
      discription: ""
    },
    {
      id: 3,
      name: "Docker",
      src: "docker.png",
      period: "",
      discription: ""
    },
    {
      id: 2,
      name: "CirclCI",
      src: "circleci.png",
      period: "",
      discription: ""
    },
    {
      id: 1,
      name: "Firebase",
      src: "firebase.png",
      period: "",
      discription: ""
    }
  ]
}
</script>
<style scoped>
.icon {
  width: 60px;
  height: 60px;
}
</style>