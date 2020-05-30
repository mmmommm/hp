<template>
    <section id="introduce" class="introduce-wrapper">
        <!-- <img class="office-image" src="@/assets/office.jpeg" alt="404 Not Found"> -->
        <div class="title-wrapper">
            <h2>ABOUT</h2>
        </div>
        <div class="introduce">
            <p>こんにちは</p>
        </div>
        <!-- 自己紹介を書く、github、twitterのアカウントのリンクを貼る -->
        <!-- <div class="explain-wrapper">
            <div class="explain" v-show="!this.$store.state.navi">
                <div class="wrapper">
                    <router-link
                    class="fancy-button bg-gradient1"
                    to="/Pastworks"><span>
                    <i class="fa fa-wheelchair-alt">
                    </i>Pastworks ></span></router-link>
                </div>
                <div class="wrapper">
                    <router-link
                    class="fancy-button bg-gradient1"
                    to="/Employee"><span>
                    <i class="fa fa-wheelchair-alt">
                    </i>Staff introduction ></span></router-link>
                </div>
            </div>
        </div> -->
    </section>
</template>

<script　lang="ts">
import { Vue, Component} from 'vue-property-decorator';
@Component
export default class About extends Vue{}
</script>

<style scoped>
section{
    padding-top: 30px;
    z-index: -1;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}
.office-image{
    padding-top: 50px;
    margin-left: 10px;
    position: absolute;
    width: 550px;
    height: auto;
    z-index: -1;
}
.title-wrapper{
    display: inline-block;
    margin-top: 50px;
    margin-left: 650px;
}
.title-wrapper h2{
    color: black;
    padding: 10px;
    text-align: center;
    font-size: 36px;
    font-family: 'Alegreya Sans SC', sans-serif;
}
section #introduce{
    height: 900px;
    /* margin-top: 10px; */
}
.introduce{
    position: absolute;
    margin-top: 40px;
    padding: 0 20px  10px 20px;
    margin-left: 600px;
    background-color: #D3D3D3;
    z-index: -1;
}
.introduce p{
    margin-top: 20px;
}
.explain-wrapper{
    padding-top: 330px;
    margin-top: 60px;
    margin-left: 600px;
    display: flex;
}
.explain{
    /* margin-left: 50px; */
    font-size: 24px;
    display: flex;
}
.bg-gradient1 span,
.bg-gradient1:before {
  background: #222222;
  background: linear-gradient(to right, #222222 0%, #222222 80%, #222222 100%);
}
.wrapper {
  /* margin: 5% auto; */
  -webkit-transform-style: perserve-3d;
          transform-style: perserve-3d;
  /* perspecive: 800px; */
}
router-link {
  text-decoration: none;
}
router-link:hover, router-link:focus, router-link:active {
  text-decoration: none;
}
/* fancy Button */
.fancy-button {
  display: inline-block;
  margin: 30px;
  font-family: 'Montserrat', Helvetica, Arial, sans-serif;
  font-size: 17px;
  letter-spacing: 0.03em;
  text-transform: uppercase;
  color: #ffffff;
  position: relative;
}
.fancy-button:before {
  content: '';
  display: inline-block;
  height: 40px;
  position: absolute;
  bottom: -5px;
  left: 30px;
  right: 30px;
  z-index: -1;
  border-radius: 30em;
  -webkit-filter: blur(20px) brightness(0.95);
          filter: blur(20px) brightness(0.95);
  -webkit-transform-style: preserve-3d;
          transform-style: preserve-3d;
  transition: all 0.3s ease-out;
}
.fancy-button i {
  margin-top: -1px;
  margin-right: 20px;
  font-size: 1.265em;
  vertical-align: middle;
}
.fancy-button span {
  display: inline-block;
  padding: 18px 60px;
  border-radius: 50em;
  position: relative;
  z-index: 2;
  will-change: transform, filter;
  -webkit-transform-style: preserve-3d;
          transform-style: preserve-3d;
  transition: all 0.3s ease-out;
}
.fancy-button:focus, .fancy-button:active {
  color: #ffffff;
}
.fancy-button:hover {
  color: #ffffff;
}
.fancy-button:hover span {
  -webkit-filter: brightness(1.05) contrast(1.05);
          filter: brightness(1.05) contrast(1.05);
  -webkit-transform: scale(0.95);
          transform: scale(0.95);
}
.fancy-button:hover:before {
  bottom: 0;
  -webkit-filter: blur(10px) brightness(0.95);
          filter: blur(10px) brightness(0.95);
}
.fancy-button.pop-onhover:before {
  opacity: 0;
  bottom: 10px;
}
.fancy-button.pop-onhover:hover:before {
  bottom: -7px;
  opacity: 1;
  -webkit-filter: blur(20px);
          filter: blur(20px);
}
.fancy-button.pop-onhover:hover span {
  -webkit-transform: scale(1.04);
          transform: scale(1.04);
}
.fancy-button.pop-onhover:hover:active span {
  -webkit-filter: brightness(1) contrast(1);
          filter: brightness(1) contrast(1);
  -webkit-transform: scale(1);
          transform: scale(1);
  transition: all 0.15s ease-out;
}
.fancy-button.pop-onhover:hover:active:before {
  bottom: 0;
  -webkit-filter: blur(10px) brightness(0.95);
          filter: blur(10px) brightness(0.95);
  transition: all 0.2s ease-out;
}
</style>