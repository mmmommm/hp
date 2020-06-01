<template>
    <section class="pt-8">
        <div class="title-wrapper mx-auto py-6">

            <h1>KISSE PORTFOLIO</h1>
        </div>
            <ul class="flex mx-auto box mt-8">
                <h4 class="w-1/4 mt-4">CONTACT</h4>
                <li class="w-1/4"><nuxt-link to="/contact" ><img src="~/assets/icon/gmail.svg" alt=""></nuxt-link></li>
                <li class="w-1/4"><a href="https://github.com/mmmommm/" alt="" target="_blank"><img src="~/assets/icon/github.jpg" alt=""></a></li>
                <li class="w-1/4"><a href="https://twitter.com/kissessenose" target="_blank"><img src="~/assets/icon/twitter.png" alt=""></a></li>
            </ul>
    </section>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";
@Component
export default class Footer extends Vue {};
</script>
<style scoped>
section{
    background-color: #222222;
    height: 300px;
}
h1{
    font-size: 36px;
    font-family:  'Alegreya Sans SC', sans-serif;
    color: white;
    text-align: center;
}
h4{
    color: white;
}
li{
    list-style: none;
}

img{
    width: 60px;
    height: 60px;
    border-radius: 15%;
}
.title-wrapper{
    background-color: black;
    height: 100px;
    width: 500px;
}
.box {
    width: 500px;
}
</style>
