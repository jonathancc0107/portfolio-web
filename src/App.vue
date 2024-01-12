<template>
  <div class="min-h-screen w-full bg-neutral-950 bg-[radial-gradient(ellipse_80%_80%_at_50%_-20%,rgba(120,119,198,0.3),rgba(255,255,255,0))]">
    <topbar></topbar>
    <router-view></router-view>
  </div>
</template>

<script setup>
import Topbar from './components/Topbar.vue';
import { onMounted } from 'vue';
import { initFlowbite } from 'flowbite';

onMounted(() => {
  initFlowbite();
})

</script>