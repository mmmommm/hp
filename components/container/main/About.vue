<template>
    <section id="about">
      <div class="introduce-wrapper lg:flex pt-6 md:pt-0">
        <div class="w-full lg:w-1/2">
          <div class="title-wrapper ml-24 md:mt-24 md:ml-48">
              <h1>ABOUT</h1>
          </div>
          <transition appear>
            <div class="mt-4 px-4 md:ml-24">
                <p class="mt-4 md:text-base">
                  同志社大学商学部三回きっせです。簿記会計・企業経営を<br>
                  専攻しておりマーケティングのゼミに所属しています。<br>
                  元々この学部に入った理由は株式投資に興味があったから<br>
                  なので現在少額ですが取引を行っています。<br>
                  文系ですがプログラミング学んでおりエンジニアとして就職する予定です。<br>
                  高校時代の友人と長期休暇を用いて自転車旅をしており<br>
                  上に表示されている画像は九州一周をしたときの写真です。
                </p>
            </div>
          </transition>
          <div class="flex mx-2 link-wrapper mt-8 ml-12 md:ml-48 md:w-full">
            <div class="sm:w-1/3 lg:w-1/6">
              <a href="https://github.com/mmmommm/" target="_blank">
                <button class="py-2 px-4 rounded">
                  <img src="~/assets/icon/github.jpg" alt="" class="github">
                </button>
              </a>
            </div>
            <div class="sm:w-1/3 lg:w-1/6">
              <a href="https://twitter.com/kissessenose" target="_blank">
                <button class="py-2 px-4 rounded">
                  <img src="~/assets/icon/twitter.png" alt="" class ="twitter">
                </button>
              </a>
            </div>
            <div class="sm:w-1/3 lg:w-1/6 ml-4 md:ml-0 mt-2">
              <nuxt-link to="/aboutDetail">
                <button class="duration-500 ease-in-out bg-transparent text-black-700 font-semibold hover:text-white hover:bg-gray-600 py-2 px-4 border border-black-500 rounded">
                  more ＞
                </button>
              </nuxt-link>
            </div>
          </div>
        </div>
        <div class="hidden md:block lg:w-1/2 lg:ml-12">
          <img src="~/assets/image/profile.JPG" alt="" class="profileImage">
        </div>
        <div class="mt-4 ml-12 md:hidden">
          <img src="~/assets/image/circleImage.png" alt="">
        </div>
      </div>
      <div class="hidden md:block" id="box1"></div>
      <div class="hidden md:block" id="box2"></div>
    </section>
</template>
<script　lang="ts">
import { Vue, Component} from 'vue-property-decorator';
@Component
export default class About extends Vue{}
</script>

<style scoped>
.v-enter, .v-leave-to {
  opacity: 0;
}
.v-enter-to, .v-leave {
  opacity: 1;
}
.v-enter-active, .v-leave-active {
  transition: 5s;
}
section{
    padding-top: 30px;

}
.title-wrapper h1{
  color: black;
  padding: 10px;
  text-align: center;
  font-size: 60px;
  font-family: 'Alegreya Sans SC', sans-serif;
}
.introduce-wrapper {
  margin-bottom: 200px;
}
.github {
  height: 40px;
  width: 40px;
}
.twitter {
  height: 40px;
  width: 40px;
}
.profile {
  height: 200px;
  width: 200px;
}
.profileImage {
  width: auto;
  height: 600px;
}
#box1 #box2 {
  height: 100px;
}
#box1 {
  position: relative;
  background-color: white;
  margin-top: 100px;
}
#box1::before {
  content:"";
  position: absolute;
  z-index: -1;
  bottom: 0;
  left: 0;
  width: 0;
  height: 0;
  border-style: solid;
/*ここで三角形のサイズを決める。
  必ず幅100vwにして、ブラウザサイズいっぱいにしてください。*/
  border-width: 100px 50vw ;
  border-color: transparent black black transparent;
}
</style>