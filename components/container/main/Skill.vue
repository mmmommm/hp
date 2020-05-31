<template>
  <section id="skill">
    <div class="bg-black">
      <div class="title-wrapper mx-auto">
        <h1>SKILL</h1>
      </div>
      <div
        class="flex justify-between"
        v-for="(skillCard, i) in skillCards"
        :key="i"
      >
        <div class="w-1/4 rounded border-white">
          <nuxt-link to="">
            <img src="" alt="">
            <p class="skillName">{{ skillCard.name }}</p>
          </nuxt-link>
        </div>
      </div>
    </div>
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
      src: ""
    },
    {
      name: "CSS",
      src: ""
    },
    {
      name: "Typescript",
      src: ""
    },
    {
      name: "Vue/Nuxt",
      src: ""
    },
    {
      name: "GitHub",
      src: ""
    },
    {
      name: "Docker",
      src: ""
    },
    {
      name: "CirclCI",
      src: ""
    },
    {
      name: "Firebase",
      src: ""
    },
  ]
}
</script>
<style scoped>
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
</style>