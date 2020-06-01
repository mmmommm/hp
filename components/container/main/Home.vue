<template>
  <section id="home" class="home-wrapper">
     <div class="container w-full mx-auto">
       <br>
       <button @click="show = !show">osite</button>
        <transition-group appear name="list" tag="div" class="flex flex-wrap justify-between" mode="out-in">
            <div
              v-for="(name, i) in names"
              :key="name.id"
              class="w-1/4 px-4 py-4 border-2 border-white card"
              :style="{
                transitionDelay: `${i * 500}ms`
              }"
            >
              <div v-if="show">
                <nuxt-link to="/skillIndex">
                  <div class="flex">
                    <p class="skillName my-auto w-1/2">{{ name.name }}</p>
                  </div>
                </nuxt-link>
              </div>
            </div>
        </transition-group>
     </div>
    <!-- <img src="~/assets/bicycle.JPG" alt=""> -->
  </section>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
export interface name {
  id: number
  name: string
}
@Component
export default class Home extends Vue{
  show = true
  names: name[] = [
    {
      id: 1,
      name: "HTML",
      
    },
    {
      id: 2,
      name: "CSS",
      
    },
    {
      id: 3,
      name: "Typescript",
      
    },
    {
      id: 4,
      name: "Vue/Nuxt",
      
    },
    {
      id: 5,
      name: "GitHub",
      
    },
    {
      id: 6,
      name: "Docker",
      
    },
    {
      id: 7,
      name: "CirclCI",
      
    },
    {
      id: 8,
      name: "Firebase",
      
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
#home {
  height:600px
}
</style>