<template>
  <section id="work" class="home-wrapper">
    <div class="title-wrapper pb-8">
      <h1>WORK</h1>
    </div>
    <!-- 将来的に公開するものが増えたらv-forで回す -->
    <div class="flex mx-4 my-4 py-2 border-2 border-black rounded">
      <div class="lg:w-1/2">
        <img src="~/assets/image/work.png" alt="" class="workImage">
      </div>
      <div class="lg:w-1/2">
        <a href="https://horizontal-ward-253909.web.app/" target="_blank">
          <p class="title">{{ this.title }}　＜＝</p>
        </a>
        <p class="content mt-4 mr-4">{{ this.content }}</p>
      </div>
    </div>
  </section>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
@Component
export default class Work extends Vue {
    title = "BRAND MEMO"
    content = "株式投資の銘柄を選ぶために企業の分析やチャートの状態についてメモできるように作ったウェブサイトです。"
    url = ""
}
</script>
<style scoped>
#work {
  height:600px
}
.title {
  font-size: 30px;
  margin-right: 250px;
}
.content {
  font-size: 18px;
}
.title-wrapper h1{
  text-align: right;
  margin-right: 300px;
    color: black;
    padding: 10px;
    font-size: 60px;
    font-family: 'Alegreya Sans SC', sans-serif;
}
.workImage {
  margin-left: 50px;
  width: 600px;
  height: auto;
}
</style>