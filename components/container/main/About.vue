<template>
  <section id='about' class='bg-pink-100'>
    <div class='introduce-wrapper lg:flex pt-6 md:pt-0'>
      <div class='w-screen lg:w-1/2'>
        <div id='about-start' class="about-start">
          <div class='text-5xl md:text-6xl text-center md:mt-24 md:ml-48 text-gray-700 font-mono'>
            <h1>ABOUT</h1>
          </div>
          <div class='mt-4 px-4 md:ml-24 box text-gray-700'>
            <p class='mt-4 md:text-base'>
              同志社大学商学部三回きっせです。簿記会計・企業経営を<br>
              専攻しておりマーケティングのゼミに所属しています。<br>
              元々この学部に入った理由は株式投資に興味があったから<br>
              なので現在少額ですが取引を行っています。<br>
              文系ですがプログラミング学んでおりエンジニアとして就職する予定です。<br>
              高校時代の友人と長期休暇を用いて自転車旅をしており<br>
              上に表示されている画像は九州一周をしたときの写真です。
            </p>
          </div>
          <div class='flex mx-2 link-wrapper mt-8 ml-12 md:ml-48 md:w-full'>
            <div class='sm:w-1/3 lg:w-1/6'>
              <a href='https://github.com/mmmommm/' target='_blank'>
                <button class='py-2 px-4 rounded hover:opacity-75'>
                  <img src='~/assets/icon/github.jpg' data-src='~/assets/icon/github.jpg' alt='githubのアイコン' class='github'>
                </button>
              </a>
            </div>
            <div class='sm:w-1/3 lg:w-1/6'>
              <a href='https://twitter.com/kissessenose' target='_blank'>
                <button class='py-2 px-4 rounded hover:opacity-75'>
                  <img src='~/assets/icon/twitter.png' data-src='~/assets/icon/twitter.png' alt='twitterのアイコン' class ='twitter'>
                </button>
              </a>
            </div>
            <div class='sm:w-1/3 lg:w-1/6 ml-4 md:ml-0 mt-2'>
              <nuxt-link to='/aboutDetail'>
                <button class='duration-500 ease-in-out bg-transparent text-black-700 font-semibold hover:bg-pink-200 py-2 px-4 border border-black-500 rounded'>
                  more ＞
                </button>
              </nuxt-link>
            </div>
          </div>
        </div>
      </div>
      <div class='hidden md:block lg:w-1/2 lg:ml-12'>
        <img src='~/assets/image/profile.JPG' data-src='~/assets/image/profile.JPG' alt='伏見稲荷で撮った画像' class='profileImage'>
      </div>
      <div class='mt-4 ml-12 md:hidden'>
        <img src='~/assets/image/circleImage.png' data-src='~/assets/image/circleImage.png' alt='伏見稲荷で撮った画像を丸く切り抜いたもの' class="circleImage">
      </div>
    </div>
    <div id='box1' class='w-screen'></div>
    <div id='box2' class='w-screen'></div>
  </section>
</template>
<script lang='ts'>
import { Vue, Component, Watch } from 'vue-property-decorator';
import 'lazysizes'
@Component
export default class About extends Vue{
  positionY = 0
  positions = {
    second: 0
  }
  mounted() {
    window.addEventListener('scroll', this.checkScroll)
    if (document != null) {
      this.positions = {
        second: document.getElementById('about').getBoundingClientRect().top
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
      let el = document.getElementById('about-start')
      if (el != null) {
        el.setAttribute('class', 'aboutAnime')
      }
    }
  }
}
</script>
<style scoped>
section{
    padding-top: 30px;
}
.introduce-wrapper {
  margin-bottom: 200px;
}
.github, .lazyloading {
  height: 40px;
  width: 40px;
}
.twitter, .lazyloading {
  height: 40px;
  width: 40px;
}
.profile, .lazyloading {
  height: 200px;
  width: 200px;
}
.profileImage, .lazyloading {
  width: auto;
  height: 600px;
}
.circleImage, .lazyloading {
  width: auto;
  height: 150px;
}
.about-start {
  opacity: 0;
}
.aboutAnime {
  transition: all 1s 0s ease;
  opacity: 1;
}
#box1 #box2 {
  height: 100px;
}
#box1 {
  position: relative;
  background-color: #FFF5F7;
  margin-top: 100px;
}
#box1::before {
  content:'';
  position: absolute;
  z-index: -1;
  bottom: 0;
  left: 0;
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 100px 50vw ;
  border-color: #FFF5F7 #1A202C #1A202C #FFF5F7;
}
</style>