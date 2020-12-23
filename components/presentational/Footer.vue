<template>
  <section class='py-8 bg-red-200 md:px-64'>
    <div class='h-24 mx-auto py-8 bg-pink-100'>
        <h1 class='text-2xl md:text-3xl text-gray-700 font-mono'>KISSE PORTFOLIO</h1>
    </div>
    <footer class="text-gray-700 text-center pt-6 text-xs md:text-xl">
        Copyright©︎2020 KISSEPORTFOLIO All Rights Reserved
    </footer>
  </section>
</template>

<script lang='ts'>
import { Vue, Component } from 'vue-property-decorator';
@Component
export default class Footer extends Vue {};
</script>
<style scoped>
h1{
    text-align: center;
}
h4{
    color: white;
}
img{
    width: 60px;
    height: 60px;
    border-radius: 15%;
}
</style>
