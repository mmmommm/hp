<template>
  <div class='h-full w-screen'>
    <div class='pt-24 md:pt-16 bg-pink-100'>
      <h1 class='text-4xl md:text-5xl text-gray-700 ml-16 md:ml-24 font-mono'>ABOUT</h1>
      <div class='mt-4 px-4 py-6 md:ml-24'>
        <p class='mt-4 text-gray-700 md:text-base about-first'>
          同志社大学商学部三回きせです。<br>
          簿記会計・企業経営を専攻しておりマーケティングのゼミに所属しています。
        </p><br>
        <p class='text-gray-700 md:text-base about-second'>
          元々この学部に入った理由は株式投資に興味があったからなので現在少額ですが取引を行っています。<br>
          簿記会計は決算短信などを読み解くために企業経営は純粋な興味から選びました。<br>
          株式投資なら金融なんじゃないの？と思われるかも知れないですがPBRとかPERとかの金融系の知識覚えるよりは実践して先物手口とか板読みとかを覚えた方が良いし、<br>
          どうせ独学できる範囲だろうという判断で選びませんでした。企業経営の概念とかは本とかでは身につかないような気がしたのも理由です。
        </p><br><br>
        <p class='text-gray-700 md:text-base about-third'>
          文系ですが友達から誘われてプログラミングスクールに通ったのがこの世界に触れるようになったきっかけです、今はエンジニアとしての就職を考えています。<br>
        </p><br>
        <p class='text-gray-700 md:text-base about-fourth'>
          気になる技術としては最近はウェブパフォーマンスに興味があります。
        </p><br><br>
        <p class='text-gray-700 md:text-base about-fifth'>
          22卒の予定ですが、気が変わって休学とかしたら23卒になるかも知れないです。
        </p><br>
        <p class='text-gray-700 md:text-base about-sixth'>
          趣味は自転車乗ることとテニスすることでホームに表示されている画像は自転車で九州一周をしたときの写真です。<br>
          好きなアーティストはKingGnuと緑黄色社会です！！！
        </p><br>
        <p class='text-gray-700 md:text-base about-last'>
          あー毎日ステーキ食べたい。。。
        </p><br>
      </div>
    </div>
  </div>
</template>
<script lang='ts'>
import { Vue, Component } from 'vue-property-decorator'
import { gsap } from 'gsap'
@Component
export default class AboutDetail extends Vue {
  mounted() {
    gsap.from('.about-first', { duration:0.5, opacity: 0 })
    gsap.from('.about-second', { duration:0.5, delay: 0.5, opacity: 0 })
    gsap.from('.about-third', { duration:0.5, delay: 1, opacity: 0 })
    gsap.from('.about-fourth', { duration:0.5, delay: 1.5,  opacity: 0 })
    gsap.from('.about-fifth', { duration:0.5, delay: 2,  opacity: 0 })
    gsap.from('.about-sixth', { duration:0.5, delay: 2.5,  opacity: 0 })
    gsap.from('.about-last', { duration:0.5, delay: 4, ease: 'bounce.out',y: -200, opacity: 0 })
  }
}
</script>