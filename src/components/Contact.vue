<template>
  <section id="contact" class="section mx-auto lg:w-[740px] w-full pb-24">
    <div class="mb-5">
      <h1 class="text-2xl text-white font-bold mb-3">
        <span class="material-icons-outlined align-middle">email</span>
        {{ $t('home.social.titles[0]') }}
      </h1>
      <div class="flex gap-4">
        <input class="border text-gray-900 text-sm rounded-lg block w-full p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white" ref="inputRef" type="text" value="jonathancaballeroc0107@gmail.com" disabled>
        <a href="mailto:jonathancaballeroc0107@gmail.com" class="text-white border border-gray-300 transition hover:scale-110 hover:bg-white hover:text-gray-700 rounded-lg p-2" target="_blank"><span class="material-icons-outlined align-middle">edit</span></a>
        <button class="text-white border border-gray-300 transition hover:scale-110 hover:bg-white hover:text-gray-700 rounded-lg p-2" @click="copyText"><span class="material-icons-outlined align-middle">content_copy</span></button>
      </div>
    </div>
    <div>
      <h1 class="text-2xl text-white font-bold mb-3">
        <span class="material-icons-outlined align-middle">person</span>
        {{ $t('home.social.titles[1]') }}
      </h1>
      <div class="flex gap-4 flex-wrap">
        <SocialPill :href="social.href" v-for="social in socials" :key="'social-'+social.name">
          <component class="size-6" :is="social.icon"></component>
          {{ social.text }}
        </SocialPill>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';
import SocialPill from './SocialPill.vue';
import GitHub from './icons/GitHub.vue';
import LinkedIn from './icons/LinkedIn.vue';

const inputRef = ref(null);

const socials = [
  {
    name: 'LinkedIn',
    href: 'https://www.linkedin.com/in/jonathan-caballero-castillo-086918175/',
    icon: LinkedIn,
    text: 'Linkedin',
  }, 
  {
    name: 'GitHub',
    href: 'https://github.com/jonathancc0107',
    icon: GitHub,
    text: 'GitHub',
  },
];

const copyText = () => {
  navigator.clipboard.writeText('jonathancaballeroc0107@gmail.com')
}
</script>
