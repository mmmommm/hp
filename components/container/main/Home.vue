<template>
  <section id="home" class="home-wrapper">
    <img src="~/assets/image/bicycle.jpeg" alt="" class="homeImage">
  </section>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator';
@Component
export default class Home extends Vue {}
</script>
<style scoped>
#home {
  height:800px
}
.homeImage {
  width: 100%;
  height: auto;
}
</style>