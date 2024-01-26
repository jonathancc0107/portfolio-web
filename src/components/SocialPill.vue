<template>
  <a class="text-white  
  border border-gray-300 rounded-full
  transition hover:scale-110
  hover:bg-white hover:text-gray-700
  flex gap-4 justify-center items-center
  py-1 px-2 md:py-2 md:px-4" :href="props.href" target="_blank">
    <slot />
  </a>
</template>

<script setup>
const props = defineProps({
  href: String,
});
</script>

