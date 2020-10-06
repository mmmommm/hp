<template>
  <div class='pt-24 md:pt-16 bg-white w-full mx-auto max-w-sm md:max-w-lg'>
    <h1 class='text-4xl md:text-5xl text-gray-700'>CONTACT</h1>
    <h4 class='text-gray-700 md:ml-12 mt-4'>何かありましたらryota1839[at]gmail.comにご連絡ください。</h4>
    <ul class='text-center font-mono mt-4'>
      <li v-for='(link, i) in links' :key='i' class='h-16 pt-4 my-8 hover:bg-red-200'>
        <a :href='link.href' target='_blank' class='text-2xl text-gray-800' rel='noopener noreferrer'>
            {{ link.title }}
        </a>
      </li>
    </ul>
  </div>
</template>
<script lang='ts'>
import { Vue, Component } from 'vue-property-decorator';
import { contactData } from '~/interface/contact';
export default class contact extends Vue {
  links: contactData[] = [
    {
      id: 1,
      title: 'GitHub',
      href: 'https://github.com/mmmommm'
    },
    {
      id: 2,
      title: 'Twitter',
      href: 'https://twitter.com/kissessenose'
    },
    {
      id: 3,
      title: 'Qiita',
      href: 'https://qiita.com/mmomm'
    },
    {
      id: 4,
      title: 'Wantedly',
      href: 'https://www.wantedly.com/users/109825255'
    },
  ]
}
</script>