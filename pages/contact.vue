<template>
  <div class='pt-24 md:pt-16 bg-white w-full mx-auto max-w-sm md:max-w-lg'>
    <h1 class='text-4xl md:text-5xl ml-2 md:ml-0 text-gray-700'>CONTACT</h1>
    <h4 class='text-gray-700 ml-4 md:ml-0 mt-4'>何かありましたらryota1839[at]gmail.comにご連絡ください。</h4>
    <div class='text-center flex flex-wrap font-mono mt-4'>
      <div v-for='(link, i) in links' :key='i' class='h-16 md:h-32 pt-4 md:pt-12 my-8 w-full md:w-1/2'>
        <a :href='link.href' target='_blank' :class='link.class' rel='noopener noreferrer'>
            {{ link.title }}
        </a>
      </div>
    </div>
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
      href: 'https://github.com/mmmommm',
      class: 'text-2xl text-black transition duration-500 ease-in-out hover:scale-90'
    },
    {
      id: 2,
      title: 'Twitter',
      href: 'https://twitter.com/kissessenose',
      class: 'text-2xl text-blue-300'
    },
    {
      id: 3,
      title: 'Qiita',
      href: 'https://qiita.com/mmomm',
      class: 'text-2xl text-green-500'
    },
    {
      id: 4,
      title: 'Zenn',
      href: 'https://zenn.dev/mmomm',
      class: 'text-2xl text-blue-500'
    },
    {
      id: 5,
      title: 'Wantedly',
      href: 'https://www.wantedly.com/users/109825255',
      class: 'text-2xl text-blue-700'
    },
    {
      id: 6,
      title: 'LAPRAS',
      href: 'https://lapras.com/public/LU7IGQD',
      class: 'text-2xl text-blue-900'
    }
  ]
}
</script>