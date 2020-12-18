<template>
  <section>
    <div>
      <header class='text-gray-700'>
        <div class='h-16 px-2 flex justify-between items-center w-screen fixed bg-red-200 md:px-12'>
          <h1 class='text-2xl font-semibold md:text-l text-gray-700 font-mono'>KISSE PORTFOLIO</h1>
          <div class='hidden md:block'>
            <ul class='md:flex md:mr-12'>
              <nuxt-link to='/' class='px-8 hover:bg-pink-100 transition duration-500 ease-in-out'>
                <li class='h-16 w-16 pt-4 border-b md:border-none pl-2 font-mono'>
                  Home
                </li>
              </nuxt-link>
              <nuxt-link to='/aboutDetail' class='px-8 hover:bg-pink-100 transition duration-500 ease-in-out'>
                <li class='h-16 w-16 pt-4 border-b md:border-none pl-2 font-mono'>
                  About
                </li>
              </nuxt-link>
              <nuxt-link to='/skillDetail' class='px-8 hover:bg-pink-100 transition duration-500 ease-in-out'>
                <li class='h-16 w-16 pt-4 border-b md:border-none pl-2 font-mono'>
                  Skill
                </li>
              </nuxt-link>
              <nuxt-link to='/contact' class='px-8 hover:bg-pink-100 transition duration-500 ease-in-out'>
                <li class='h-16 w-16 pt-4 border-b md:border-none font-mono'>
                  Contact
                </li>
              </nuxt-link>
            </ul>
          </div>
          <button @click='activeToggle' class='md:hidden' aria-label="hamburger menu">
            <transition name='navi'>
              <svg class='h-6 w-6 fill-current' viewBox='0 0 24 24'>
                <path v-show='!active' d='M24 6h-24v-4h24v4zm0 4h-24v4h24v-4zm0 8h-24v4h24v-4z'/>
                <path v-show='active' d='M24 20.188l-8.315-8.209 8.2-8.282-3.697-3.697-8.212 8.318-8.31-8.203-3.666 3.666 8.321 8.24-8.206 8.313 3.666 3.666 8.237-8.318 8.285 8.203z'/>
              </svg>
            </transition>
          </button>
        </div>
        <transition name='navi'>
          <div v-show='active' class='mt-16 fixed h-60 w-48 bg-red-300 right-0 mr-4'>
            <ul class='text-center font-mono'>
              <nuxt-link to='/' class='text-2xl text-gray-800'>
                <li @click='activeOff' class='h-16 pt-4'>
                  Home
                </li>
              </nuxt-link>
              <nuxt-link to='/aboutDetail' class='text-2xl text-gray-800'>
                <li @click='activeOff' class='h-16 pt-4'>
                  About
                </li>
              </nuxt-link>
              <nuxt-link to='/skillDetail' class='text-2xl text-gray-800'>
                <li @click='activeOff' class='h-16 pt-4'>
                  Skill
                </li>
              </nuxt-link>
              <nuxt-link to='/contact' class='text-2xl text-gray-800'>
                <li @click='activeOff' class='h-16 pt-4'>
                  Contact
                </li>
              </nuxt-link>
            </ul>
          </div>
        </transition>
      </header>
    </div>
  </section>
</template>

<script lang='ts'>
import { Vue, Component } from 'vue-property-decorator';
@Component
export default class Header extends Vue{
  active = false
  readonly HEADER_MAX_HEIGHT = 60
  isOpen = true
  height() {
    return this.isOpen ? this.HEADER_MAX_HEIGHT : 0;
  }
  itemStyle() {
    const opacity = this.isOpen ? 1 : 0;
    const scale   = this.isOpen ? 1 : 0;
    return {
      height: `${this.height}px`,
      transform: `scale(${scale}, ${scale})`,
      opacity,
    };
  }
  headStyle() {
    return {
      height: `${this.height}px`,
      background: this.isOpen ? '#fff' : '#fefef0',
    };
  }
  activeToggle() {
    this.active = !this.active
  }
  activeOff() {
    this.active = false
  }
}
</script>

<style scoped>
div {
  z-index: 1000;
}
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