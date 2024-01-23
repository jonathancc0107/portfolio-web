<template>
  <div class="absolute w-3 h-3 bg-gray-500 rounded-full mt-1.5 -start-1.5 border border-gray-900"></div>
  <time class="mb-1 text-sm font-normal leading-none text-gray-500">{{ period }}</time>
  <h3 class="text-lg font-semibold text-white">{{ position }} - {{ company }}</h3>
  <p class="mb-4 text-base font-normal text-gray-400">{{ description }}</p>
</template>

<script setup>
const props = defineProps({
  company: String,
  description: String,
  period: String,
  position: String,
});
</script>
