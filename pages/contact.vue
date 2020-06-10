<template>
  <div class="pt-24 md:pt-16 bg-white w-full mx-auto max-w-sm md:max-w-lg">
    <h1 class="text-4xl md:text-5xl text-black">CONTACT</h1>
    <form class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4">
      <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="name">
          名前/name
        </label>
        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" type="text" placeholder="yourname">
      </div>
      <div class="mb-6">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
          メールアドレス/Email
        </label>
        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 mb-3 leading-tight focus:outline-none focus:shadow-outline" id="password" type="email" placeholder="your email">
      </div>
      <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="name">
          件名/Subject
        </label>
        <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="your subject">
      </div>
      <div class="mb-4">
        <label class="block text-gray-700 text-sm font-bold mb-2" for="name">
          内容/Body
        </label>
        <textarea class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="body"/>
      </div>
      <div class="flex items-center">
        <div class="w-1/3"></div>
        <div class="w-2/3">
          <button class="shadow text-black hover:text-white bg-white hover:bg-black focus:shadow-outline focus:outline-none font-bold py-2 px-4 rounded" type="button">
            送信/submit
          </button>
        </div>
      </div>
    </form>
  </div>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'
export default class contact extends Vue {}
</script>