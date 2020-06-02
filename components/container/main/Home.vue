<template>
  <section id="home" class="md:h-screen">
    <div class="hidden md:block">
      <img src="~/assets/image/bicycle.jpeg" alt="" class="homeImage">
    </div>
    <div class="md:hidden">
      <img src="~assets/image/homeImage.jpeg" alt="">
    </div>
  </section>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
@Component
export default class Home extends Vue {}
</script>
<style scoped>
.homeImage {
  width: 100%;
  height: auto;
}
</style>