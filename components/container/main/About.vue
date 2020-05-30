<template>
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
          <div class="lg:w-1/3">
            <nuxt-link to="">
              <button class="bg-transparent text-black-700 font-semibold hover:text-white py-2 px-4 border border-black-500 hover:border-transparent rounded">
                <img src="~/assets/github.jpg" alt="">
              </button>
            </nuxt-link>
          </div>
          <div class="lg:w-1/3">
            <nuxt-link to="">
              <button class="bg-transparent text-black-700 font-semibold hover:text-white py-2 px-4 border border-black-500 hover:border-transparent rounded">
                <img src="~/assets/twitter.png" alt="">
              </button>
            </nuxt-link>
          </div>
          <div class="lg:w-1/3">
            <nuxt-link to="">
              <button class="bg-transparent text-black-700 font-semibold hover:text-white py-2 px-4 border border-black-500 hover:border-transparent rounded">
                more　＞
              </button>
            </nuxt-link>
          </div>
        </div>
      </div>
      <div class="lg:w-1/2">
        <img src="" alt="">
      </div>
    </section>
</template>

<script　lang="ts">
import { Vue, Component} from 'vue-property-decorator';
@Component
export default class About extends Vue{}
</script>

<style scoped>
section{
    padding-top: 30px;
    z-index: -1;
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
section #introduce{
    height: 900px;
    /* margin-top: 10px; */
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
</style>