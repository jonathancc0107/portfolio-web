<template>
  <section id="experience" class="section mx-auto lg:w-[740px] w-full">
    <h1 class="text-2xl text-white font-bold pb-5">
      <span class="material-icons-outlined align-middle">work_outline</span>
      {{ $t('home.experience.title') }} 
    </h1>
    <ol class="relative border-s border-gray-200 dark:border-gray-700">                  
      <li class="mb-10 ms-4" v-for="item in $tm('home.experience.experiences')" :key="item">
        <ExperienceItem :company="$rt(item.company)" :description="$rt(item.description)" :period="$rt(item.period)" :position="$rt(item.position)" />
      </li>
    </ol>
  </section>
</template>

<script setup>
import ExperienceItem from './ExperienceItem.vue';
</script>

