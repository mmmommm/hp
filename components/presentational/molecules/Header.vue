<template>
    <section>
      <div>
        <header class="header container mx-auto text-white">
          <div class="h-16 px-2 flex justify-between items-center fixed w-full left-0 bg-black md:px-12">
            <h1 class="text-2xl font-semibold md:text-l">KISSE PORTFOLIO</h1>
            <button @click="activeToggle" class="focus:outline-none">
              <transition name="navi">
                <svg class="h-6 w-6 fill-current" viewBox="0 0 24 24">
                  <path v-show="!active" d="M24 6h-24v-4h24v4zm0 4h-24v4h24v-4zm0 8h-24v4h24v-4z"/>
                  <path v-show="active" d="M24 20.188l-8.315-8.209 8.2-8.282-3.697-3.697-8.212 8.318-8.31-8.203-3.666 3.666 8.321 8.24-8.206 8.313 3.666 3.666 8.237-8.318 8.285 8.203z"/>
                </svg>
              </transition>
            </button>
          </div>
          <transition name="navi">
            <div v-show="active" class="mt-16 fixed w-full bg-gray-900 left-0">
              <ul class="md:flex md:justify-end py-4 md:mr-12">
                <li class="border-b md:border-none" @click="activeOff">
                  <nuxt-link to="/" class="px-8">Home</nuxt-link>
                </li>
                <li class="border-b md:border-none" @click="activeOff">
                  <nuxt-link to="/aboutDetail" class="px-8">About</nuxt-link>
                </li>
                <li class="border-b md:border-none" @click="activeOff">
                  <nuxt-link to="/skillDetail" class="px-8">Skill</nuxt-link>
                </li>
                <!-- <li class="border-b md:border-none" @click="activeOff">
                  <nuxt-link to="/contact" class="px-8">Contact</nuxt-link>
                </li> -->
              </ul>
            </div>
          </transition>
        </header>
      </div>
    </section>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";
@Component
export default class Header extends Vue{
  active = false
  activeToggle() {
    this.active = !this.active
  }
  activeOff() {
    this.active = false
  }
}
</script>

<style scoped>
.navi-enter, .navi-leave-to {
  opacity: 0;
}
.navi-enter-to, .navi-leave {
  opacity: 1;
}
.navi-enter-active, .navi-leave-active {
  transition: .7s;
}
</style>