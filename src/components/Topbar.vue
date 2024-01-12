<template>
  <nav class="border-gray-200 bg-transparent">
    <div class="max-w-screen-xl flex flex-wrap items-center md:justify-between justify-end mx-auto p-4">
      <div class="flex md:order-2">
        <button v-if="localeSelected" type="button" data-dropdown-toggle="language-dropdown-menu" class="inline-flex items-center font-medium justify-center px-4 py-2 text-sm text-white rounded-lg cursor-pointer hover:bg-gray-700">
          <img class="h-4 w-4 me-2" :src="getImageUrl(localeSelected.flag)" :alt="`flag-${localeSelected.lang}`">           
          {{ localeSelected.label }}
        </button>
        <div class="z-50 hidden my-4 text-base list-none divide-y divide-gray-100 rounded-lg shadow bg-gray-700" id="language-dropdown-menu">
          <ul class="py-2 font-medium" role="none">
            <li v-for="locale in languages" :key="`locale-${locale.lang}`">
              <a href="#" class="block px-4 py-2 text-sm text-gray-400 hover:bg-gray-600" role="menuitem" @click="selectLang(locale)">
                <div class="inline-flex items-center"> 
                  <img class="h-4 w-4 me-2" :src="getImageUrl(locale.flag)" :alt="`flag-${locale.lang}`">           
                  {{ locale.label }}
                </div>
              </a>
            </li>
          </ul>
        </div>
        <button data-collapse-toggle="navbar" type="button" class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm rounded-lg md:hidden focus:outline-none focus:ring-2 text-gray-400 hover:bg-neutral-700 focus:ring-gray-600" aria-controls="navbar-search" aria-expanded="false">
          <span class="sr-only">Menu</span>
          <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
          </svg>
        </button>
      </div>
      <div class="items-center justify-between hidden w-full md:flex md:w-auto md:order-1" id="navbar">
        <ul class="flex flex-col p-4 md:p-0 mt-4 font-medium border rounded-lg bg-neutral-50 md:space-x-8 rtl:space-x-reverse md:flex-row md:mt-0 md:border-0 bg-neutral-800 md:bg-neutral-900 border-gray-700">
          <li>
            <router-link to="/" class="font-inter block py-2 px-3 text-white bg-neutral-800 rounded md:bg-transparent md:p-0 hover:bg-white hover:text-neutral-800">Inicio</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import { useI18n } from 'vue-i18n';

const { locale } = useI18n();

const localeSelected = ref();

const languages = [{
  label: 'Español',
  flag: '../assets/img/ES.svg',
  lang: 'es'
}, {
  label: 'English (US)',
  flag: '../assets/img/US.svg',
  lang: 'en'
}];

onMounted(() => {
  localeSelected.value = languages.find(o => o.lang === locale.value);
});

const getImageUrl = (path) => {
  return new URL(path, import.meta.url).href;
}

const selectLang = (selected) => {
  locale.value = selected.lang;
  localeSelected.value = selected;
}

</script>
