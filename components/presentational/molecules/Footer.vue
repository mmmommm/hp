<template>
    <section class="footer-wrapper">
        <div class="title-wrapper">
            <h1>kisse</h1>
        </div>
            <h4>CONTACT ME</h4>
            <ul>
                <li><a href=""><img src="@/assets/icon/gmail.svg" alt=""></a></li>
                <li><a href="#"><img src="@/assets/icon/facebook.png" alt=""></a></li>
                <li><a href="#"><img src="@/assets/icon/twitter.png" alt=""></a></li>
                <li><a href="#"><img src="@/assets/icon/instagram.png" alt=""></a></li>
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
    height: 400px;
}
h1{
    font-size: 36px;
    font-family:  'Alegreya Sans SC', sans-serif;
    color: white;
    text-align: center;
    margin-top: 20px;
}
h4{
    color: white;
    position: absolute;
    margin-top: 220px;
    margin-left: 350px;
}
ul{
    display: flex;
    margin: 200px 0 0 450px;
    position: absolute;
}
li{
    list-style: none;
    margin-left: 40px;}

img{
    width: 60px;
    height: 60px;
    border-radius: 15%;
}
.title-wrapper{
    position: absolute;
    background-color: black;
    height: 100px;
    width: 500px;
    margin: 50px 0 0 470px;
}
</style>
