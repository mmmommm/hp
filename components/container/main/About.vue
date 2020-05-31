<template>
  <div>
    <section id="introduce" class="introduce-wrapper flex">
      <div class="lg:w-1/2">
        <div class="title-wrapper">
            <h1>ABOUT</h1>
        </div>
        <!-- 自己紹介を書く、github、twitterのアカウントのリンクを貼る -->
        <div class="introduce">
            <p>
              同志社大学商学部三回きっせです。簿記会計・企業経営を<br>
              専攻しておりマーケティングのゼミに所属しています。<br>
              元々この学部に入った理由は株式投資に興味があったから<br>
              なので現在少額ですが取引を行っています。<br>
              文系ですがプログラミング学んでおりエンジニアとして就職する予定です。
            </p>
        </div>
        <div class="flex mx-2 link-wrapper">
          <div class="lg:w-1/6">
            <nuxt-link to="">
              <button class="bg-transparent text-black-700 font-semibold hover:text-white py-2 px-4 border border-black-500 hover:border-transparent rounded">
                <img src="~/assets/icon/github.jpg" alt="" class="github">
              </button>
            </nuxt-link>
          </div>
          <div class="lg:w-1/6">
            <nuxt-link to="">
              <button class="bg-transparent text-black-700 font-semibold hover:text-white py-2 px-4 border border-black-500 hover:border-transparent rounded">
                <img src="~/assets/icon/twitter.png" alt="" class ="twitter">
              </button>
            </nuxt-link>
          </div>
          <div class="lg:w-1/6 mt-2">
            <nuxt-link to="">
              <button class="bg-transparent text-black-700 font-semibold hover:text-white py-2 px-4 border border-black-500 hover:border-transparent rounded">
                more ＞
              </button>
            </nuxt-link>
          </div>
        </div>
      </div>
      <div class="lg:w-1/2">
        <!-- <img src="~/assets/image/profile.JPG" alt="" class=""> -->
      </div>
    </section>
    <div id="box1"></div>
    <div id="box2"></div>
  </div>
</template>

<script　lang="ts">
import { Vue, Component} from 'vue-property-decorator';
@Component
export default class About extends Vue{}
</script>

<style scoped>
section{
    padding-top: 30px;
    margin-bottom: 200px;

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
    margin-left: 150px;
    z-index: -1;
}
.introduce p{
    margin-top: 20px;
    font-size: 18px;
}
.link-wrapper {
  margin-top: 20px;
  margin-left: 150px;
  width: 600px
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
#box1 #box2 {
  height: 100px;
}
#box1 {
  position: relative;
  background-color: white;
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
  border-width: 100px 100vw ;
  border-color: transparent black black transparent;
}
</style>