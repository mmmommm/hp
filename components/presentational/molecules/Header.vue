<template>
    <section id="top" class="header-wrapper">
        <h1 class="title">KISSE</h1>
        <header class="header">
            <div class="header__menu">
                <div class="header__menu__line" @click="naviToggle" :class="{'is-active': active}">
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
            </div>
        </header>
        <transition name="navi">
            <nav class="navi" v-show="this.navi">
                <ul class="navi_wrap">
                    <li class="navi_wrap_link">
                        <NuxtLink to="/main">Home</NuxtLink>
                    </li>
                    <li class="navi_wrap_link">
                        <NuxtLink to="/main">About</NuxtLink>
                    </li>
                    <li class="navi_wrap_link">
                        <NuxtLink to="/main">Work</NuxtLink>
                    </li>
                    <li class="navi_wrap_link">
                        <NuxtLink to="/main">Skill</NuxtLink>
                    </li>
                </ul>
            </nav>
        </transition>
    </section>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";
@Component
export default class Header extends Vue{
  active = false
  navi = false
  naviToggle() {
    this.active = !this.active
    this.navi = !this.navi
    // this.$store.commit('naviAction')
  }
}
</script>

<style lang="scss" scoped>
.title {
  padding-top: 50px;
  margin-left: 45px;
}
.header-wrapper{
    border-bottom: solid 1px black ;
}
section{
    height: 120px;
    background-color: white;
    z-index: 1001;
    opacity: 0.95;
}
.header {
  width: 100%;
  background: #fff;
  height: 60px;
  &__menu {
    width: 180px;
    height: 180px;
    position: fixed;
    top: 0;
    right: 0;
    &__line {
      width: 108px;
      height: 30px;
      margin-top: 45px;
      margin-left: auto;
      margin-right: auto;
      position: relative;
      cursor: pointer;
      z-index: 6;
      span {
        width: 100%;
        height: 2px;
        background: #000;
        display: block;
        transition: .6s;
        position: absolute;
        &:first-child {
          top: 0;
        }
        &:nth-child(2) {
          top: 14px;
        }
        &:last-child {
          bottom: 0;
        }
      }
      &.is-active {
        span {
          transition: .6s;
          &:first-child {
            transform: rotate(45deg);
            top: 50%;
          }
          &:nth-child(2) {
            opacity: 0;
          }
          &:last-child {
            transform: rotate(-45deg);
            top: 50%;
          }
        }
      }
    }
  }
}
.navi {
  width: 100%;
  height: 100%;
  display: flex;
  &_wrap {
    list-style-type: none;
    text-align: center;
    padding-left: 0;
    background: BLACK;
    padding: 60px 0;
    width: 100%;
    height: 500px;
    z-index: 4;
    &_link {
        text-decoration: none;
        padding: 50px 0;
        z-index: 5;
        color: white;
        font-size: 24px;
    }
  }
  &-enter, &-leave-to {
    opacity: 0;
  }
  &-enter-to, &-leave {
    opacity: 1;
  }
  &-enter-active, &-leave-active {
    transition: .6s;
  }
}
</style>