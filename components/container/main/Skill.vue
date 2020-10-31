<template>
  <section id='skill'>
    <div class='text-white text-center p-4 mx-auto md:py-8 bg-gray-900'>
      <h1 class='text-5xl md:text-6xl text-pink-100 font-mono'>SKILL</h1>
    </div>
    <div class='bg-gray-900 pb-40'>
      <div id="skill-start" class="skill-start">
        <div class="w-screen flex flex-wrap justify-center">
          <div
            v-for='(skillCard, i) in skillCards'
            :key='skillCard.id'
            :data-index='i'
            class='w-1/2 md:w-1/5 md:mr-2'
          >
            <div class='card md:border-2 border-white rounded my-2 md:px-2 py-4 transition duration-500 ease-in-out hover:bg-gray-700'>
              <nuxt-link to='/skillDetail'>
                <div class='flex ml-4 md:ml-0'>
                  <img :src="require('~/static/skill/' + skillCard.src)" alt='それぞれの技術の画像' class='w-1/2 icon' :data-src="require('~/static/skill/' + skillCard.src)" />
                  <p class='text-base md:text-2xl ml-1 md:ml-4 text-white my-auto w-1/2 text-pink-100'>{{ skillCard.name }}</p>
                </div>
              </nuxt-link>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div id='space1' class='w-screen'/>
    <div id='space2' class='w-screen'/>
  </section>
</template>
<script lang='ts'>
import { Vue, Component, Watch } from 'vue-property-decorator';
import { skillCard } from '~/interface/skillCard';
import 'lazysizes'
@Component({
})
export default class Skill extends Vue {
  positionY = 0
  positions = {
    second: 0
  }
  skillCards: skillCard[] = [
    {
      id: 1,
      name: 'HTML',
      src: 'html.png'
    },
    {
      id: 2,
      name: 'CSS',
      src: 'css.png'
    },
    {
      id: 3,
      name: 'Typescript',
      src: 'ts.png'
    },
    {
      id: 4,
      name: 'Vue/Nuxt',
      src: 'nuxt.png'
    },
    {
      id:5,
      name: 'React',
      src: 'react.jpg'
    },
    {
      id: 6,
      name: 'GitHub',
      src: 'github.jpg'
    },
    {
      id: 7,
      name: 'Docker',
      src: 'docker.png'
    },
    {
      id: 8,
      name: 'CirclCI',
      src: 'circleci.png'
    },
    {
      id: 9,
      name: 'Firebase',
      src: 'firebase.png'
    },
    {
      id: 10,
      name: 'Golang',
      src: 'go.png'
    }
  ]
  mounted() {
    window.addEventListener('scroll', this.checkScroll)
    if (document != null) {
    this.positions = {
      second: document.getElementById('skill').getBoundingClientRect().top
    }
    this.positionY++
    }
  }
  checkScroll() {
    this.positionY = window.scrollY
  }
  @Watch('positionY')
  positionYChange(to: number, from: never) {
    const scrollOffset = to + 100
    if (this.positions.second <= scrollOffset) {
      let el = document.getElementById('skill-start')
      if (el != null) {
        el.setAttribute('class', 'skillAnime')
      }
    }
  }
}
</script>
<style scoped>
.icon, .lazyloading {
  width: auto;
  height: 80px;
}
.skill-start {
  opacity: 0;
}
.skillAnime {
  transition: all 1s 0s ease;
  opacity: 1;
}
#space2 {
  height: 100px;
  position: relative;
}
#space1 {
  height: 100px;
}
#space2::before {
  content:'';
  z-index: -1;
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 100px 50vw;
  border-color: #1A202C #1A202C #FFF5F7 #FFF5F7;
}
</style>