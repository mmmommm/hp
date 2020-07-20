<template>
  <section class='py-8 bg-gray-900 md:px-64'>
    <div class='h-24 mx-auto py-8 bg-black'>
        <h1 class='text-2xl md:text-3xl text-white'>KISSE PORTFOLIO</h1>
    </div>
    <ul class='flex mt-8 mx-auto'>
        <h4 class='w-1/4 mt-4 ml-2 md:ml-0 md:mx-4'>CONTACT　ME</h4>
        <li class='w-1/4 md:px-4'><nuxt-link to='/contact' ><img src='~/assets/icon/gmail.svg' alt='メールのアイコン' class='hover:opacity-75'></nuxt-link></li>
        <li class='w-1/4 md:px-4'><a href='https://github.com/mmmommm/' alt='' target='_blank'><img src='~/assets/icon/github.jpg' alt='githubのアイコン' class='hover:opacity-75'></a></li>
        <li class='w-1/4 md:px-4'><a href='https://twitter.com/kissessenose' target='_blank'><img src='~/assets/icon/twitter.png' alt='twitterのアイコン' class='hover:opacity-75'></a></li>
    </ul>
    <footer class="text-white text-center pt-6">
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
