<template>
  <section id="skill">
    <div class="skill bg-black">
      <div class="title-wrapper mx-auto py-8">
        <h1>SKILL</h1>
      </div>
      <div class="container w-full mx-auto">
        <div class="flex flex-wrap justify-between">
          <div
            v-for="(skillCard, i) in skillCards"
            :key="i"
            class="w-1/4 px-4 py-4 border-2 border-white card">
          >
              <nuxt-link to="/skillIndex">
                <div class="flex">
                  <img :src="require('~/static/skill/' + skillCard.src)" alt="" class="w-1/2 icon"/>
                  <p class="skillName my-auto w-1/2">{{ skillCard.name }}</p>
                </div>
              </nuxt-link>
          </div>
        </div>
      </div>
    </div>
    <div id="space1"/>
    <div id="space2"/>
  </section>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
import { skillCard } from "~/interfacee/skillCard"
@Component
export default class Skill extends Vue {
  skillCards: skillCard[] = [
    {
      name: "HTML",
      src: "html.png"
    },
    {
      name: "CSS",
      src: "css.png"
    },
    {
      name: "Typescript",
      src: "ts.png"
    },
    {
      name: "Vue/Nuxt",
      src: "nuxt.png"
    },
    {
      name: "GitHub",
      src: "github.jpg"
    },
    {
      name: "Docker",
      src: "docker.png"
    },
    {
      name: "CirclCI",
      src: "circleci.png"
    },
    {
      name: "Firebase",
      src: "firebase.png"
    }
  ]
}
</script>
<style scoped>
.skill {
  height: 800px;
}
.title-wrapper h1{
    color: white;
    padding: 10px;
    text-align: center;
    font-size: 60px;
    font-family: 'Alegreya Sans SC', sans-serif;
}
.skillName {
  color: white;
  font-size: 24px
}
.icon {
  width: auto;
  height: 100px;
}
.card {
  width: 300px;
}
#space1 #space2 {
  height: 100px;
}
#space1 {
  position: relative;
  background-color: black;
}
#space1::before {
  content:"";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 0;
  border-style: solid;
 /*ここで三角形のサイズを決める。
  必ず幅100vwにして、ブラウザサイズいっぱいにしてください。*/
  border-width: 100px 100vw;
 
  border-color: transparent transparent white white;
}
</style>