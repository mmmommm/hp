<template>
  <section id="work" class="h-auto md:h-screen">
    <div class="pt-12 md:pt-24">
      <div class="pb-8">
        <h1 class="text-5xl md:text-6xl">WORK</h1>
      </div>
      <!-- 将来的に公開するものが増えたらv-forで回す -->
      <div class="md:flex mx-4 my-4 py-2 md:border-2 md:border-black md:rounded">
        <div class="w-full lg:w-1/2">
          <img src="~/assets/image/work.png" alt="brandmemoのホーム画像" class="workImage md:ml-4">
        </div>
        <div class="w-full lg:w-1/2">
          <a :href="this.url" target="_blank">
            <button class="title font-semibold py-2 px-4 rounded">
              <p class="text-lg md:text-3xl">{{ this.title }}</p>
            </button>
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
.workImage {
  width: 600px;
  height: auto;
}
.title {
  transition: all 1s 0s ease;

}
.title:hover {
  background: #ccc;
}
</style>