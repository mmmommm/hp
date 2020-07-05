<template>
  <section id="skill">
    <div class="text-white text-center p-4 mx-auto md:py-8 bg-black">
      <h1 class="text-5xl md:text-6xl">SKILL</h1>
    </div>
    <div class="w-full bg-black pb-40 flex flex-wrap justify-center">
      <div
        v-for="(skillCard, i) in skillCards"
        :key="skillCard.id"
        :data-index="i"
        class="w-1/2 md:w-1/5 md:mr-2 duration-100"
      >
        <div class="card md:border-2 border-white rounded my-2 md:px-2 py-4">
          <nuxt-link to="/skillDetail">
            <div class="flex">
              <img :src="require('~/static/skill/' + skillCard.src)" alt="それぞれの技術の画像" class="w-1/2 icon"/>
              <p class="text-base md:text-2xl ml-1 md:ml-4 text-white my-auto w-1/2">{{ skillCard.name }}</p>
            </div>
          </nuxt-link>
        </div>
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
.icon {
  width: auto;
  height: 80px;
}
#space2 {
  height: 100px;
  position: relative;
}
#space1 {
  height: 100px;
}
#space2::before {
  content:"";
  z-index: -1;
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 100px 50vw;
  border-color: black black transparent transparent;
}
</style>