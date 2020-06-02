<template>
    <section id="about">
      <div class="introduce-wrapper flex">
        <div class="lg:w-1/2">
          <div class="title-wrapper">
              <h1>ABOUT</h1>
          </div>
          <!-- 自己紹介を書く、github、twitterのアカウントのリンクを貼る -->
          <transition appear>
            <div class="introduce">
                <p>
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
          <div class="flex mx-2 link-wrapper">
            <div class="lg:w-1/6">
              <a href="https://github.com/mmmommm/" target="_blank">
                <button class="bg-transparent text-black-700 font-semibold hover:text-white py-2 px-4 rounded">
                  <img src="~/assets/icon/github.jpg" alt="" class="github">
                </button>
              </a>
            </div>
            <div class="lg:w-1/6">
              <a href="https://twitter.com/kissessenose" target="_blank">
                <button class="bg-transparent text-black-700 font-semibold hover:text-white py-2 px-4 rounded">
                  <img src="~/assets/icon/twitter.png" alt="" class ="twitter">
                </button>
              </a>
            </div>
            <div class="lg:w-1/6 mt-2">
              <a href="">
                <button class="bg-transparent text-black-700 font-semibold hover:text-white py-2 px-4 border border-black-500 hover:border-transparent rounded">
                  more ＞
                </button>
              </a>
            </div>
          </div>
        </div>
        <div class="lg:w-1/2">
          <img src="~/assets/image/profile.JPG" alt="" class="profileImage">
        </div>
      </div>
      <div id="box1"></div>
      <div id="box2"></div>
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
.title-wrapper{
    display: inline-block;
    margin-top: 50px;
    margin-left: 200px;
}
.title-wrapper h1{
    color: black;
    padding: 10px;
    text-align: center;
    font-size: 60px;
    font-family: 'Alegreya Sans SC', sans-serif;
}
.introduce{
    margin-top: 40px;
    margin-left: 100px;
}
.introduce p{
    margin-top: 20px;
    font-size: 18px;
}
.introduce-wrapper {
  margin-bottom: 200px;
}
.link-wrapper {
  margin-top: 20px;
  margin-left: 150px;
  width: 600px;
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
  margin-left: 100px;
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