<template>
  <section id="work" class="h-auto md:h-screen">
    <div class="pt-12 md:pt-24">
      <div class="title-wrapper pb-8">
        <h1>WORK</h1>
      </div>
      <!-- 将来的に公開するものが増えたらv-forで回す -->
      <div class="md:flex mx-4 my-4 py-2 md:border-2 md:border-black md:rounded">
        <div class="w-full lg:w-1/2">
          <img src="~/assets/image/work.png" alt="" class="workImage md:ml-4">
        </div>
        <div class="w-full lg:w-1/2">
          <a :href="this.url" target="_blank">
            <p class="text-lg md:text-3xl md:mr-24">{{ this.title }}　＜＝</p>
          </a>
          <p class="text-sm md:text-lg mt-4 mr-4">{{ this.content }}</p>
        </div>
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
    url = "https://horizontal-ward-253909.web.app/"
}
</script>
<style scoped>
.title-wrapper h1{
  text-align: right;
  margin-right: 300px;
  color: black;
  padding: 10px;
  font-size: 60px;
  font-family: 'Alegreya Sans SC', sans-serif;
}
.workImage {
  width: 600px;
  height: auto;
}
</style>