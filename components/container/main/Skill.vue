<template>
  <section id="skill">
    <div class="skill bg-black">
      <div class="title-wrapper mx-auto py-8">
        <h1>SKILL</h1>
      </div>
      <div class="container w-full mx-auto">
        <transition-group appear name="list" tag="div" class="flex flex-wrap justify-between" mode="out-in">
            <div
              v-for="(skillCard, i) in skillCards"
              :key="skillCard.id"
              class="w-1/4 px-4 py-4 my-2 border-2 border-white rounded card"
              :style="{
                transitionDelay: `${i * 500}ms`
              }"
            >
              <div>
                <nuxt-link to="/skillIndex">
                  <div class="flex">
                    <img :src="require('~/static/skill/' + skillCard.src)" alt="" class="w-1/2 icon"/>
                    <p class="skillName my-auto w-1/2">{{ skillCard.name }}</p>
                  </div>
                </nuxt-link>
              </div>
            </div>
        </transition-group>
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
      id: 1,
      name: "HTML",
      src: "html.png"
    },
    {
      id: 2,
      name: "CSS",
      src: "css.png"
    },
    {
      id: 3,
      name: "Typescript",
      src: "ts.png"
    },
    {
      id: 4,
      name: "Vue/Nuxt",
      src: "nuxt.png"
    },
    {
      id: 5,
      name: "GitHub",
      src: "github.jpg"
    },
    {
      id: 6,
      name: "Docker",
      src: "docker.png"
    },
    {
      id: 7,
      name: "CirclCI",
      src: "circleci.png"
    },
    {
      id: 8,
      name: "Firebase",
      src: "firebase.png"
    }
  ]
}
</script>
<style scoped>
.list-enter-active .list-leave-active {
  transition: all 1s;
  transition-delay: 0;
}
.list-enter .list-leave-to {
  opacity: 0;
  transform: translateY(30px);
}
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
  border-width: 100px 50vw;
  border-color: transparent transparent white white;
}
</style>