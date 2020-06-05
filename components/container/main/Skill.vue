<template>
  <section id="skill">
    <div class="md:h-screen bg-black pt-12 md:pt-4">
      <div class="title-wrapper mx-auto md:py-8">
        <h1>SKILL</h1>
      </div>
      <div class="w-screen">
        <transition-group appear name="list" tag="div" class="flex flex-wrap md:ml-48">
            <div
              v-for="(skillCard, i) in skillCards"
              :key="skillCard.id"
              :data-index="i"
              class="sm:w-1/2 md:w-1/5 px-1 md:px-2 py-4 mx-1 md:mr-2 my-2 border-2 border-white rounded"
              :style="{
                transitionDelay: `${i * 100}ms`
              }"
            >
              <div class="w-40">
                <nuxt-link to="/skillDetail">
                  <div class="flex">
                    <img :src="require('~/static/skill/' + skillCard.src)" alt="" class="w-1/2 icon"/>
                    <p class="text-base md:text-2xl ml-1 md:ml-4 text-white my-auto w-1/2">{{ skillCard.name }}</p>
                  </div>
                </nuxt-link>
              </div>
            </div>
        </transition-group>
      </div>
    </div>
    <div class="hidden md:block" id="space1"/>
    <div class="hidden md:block" id="space2"/>
  </section>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
import { skillCard } from "~/interface/skillCard";
@Component({
})
export default class Skill extends Vue {
  skillCards: skillCard[] = [
    {
      id: 8,
      name: "HTML",
      src: "html.png"
    },
    {
      id: 7,
      name: "CSS",
      src: "css.png"
    },
    {
      id: 6,
      name: "Typescript",
      src: "ts.png"
    },
    {
      id: 5,
      name: "Vue/Nuxt",
      src: "nuxt.png"
    },
    {
      id: 4,
      name: "GitHub",
      src: "github.jpg"
    },
    {
      id: 3,
      name: "Docker",
      src: "docker.png"
    },
    {
      id: 2,
      name: "CirclCI",
      src: "circleci.png"
    },
    {
      id: 1,
      name: "Firebase",
      src: "firebase.png"
    }
  ]
}
</script>
<style scoped>
.list-enter, .list-leave-to {
  opacity: 0;
}
.list-enter-to, .list-leave {
  opacity: 1;
}
.list-enter-active, .list-leave-active {
  transition: 10s;
}
.title-wrapper h1{
    color: white;
    padding: 10px;
    text-align: center;
    font-size: 60px;
    font-family: 'Alegreya Sans SC', sans-serif;
}
.icon {
  width: auto;
  height: 80px;
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