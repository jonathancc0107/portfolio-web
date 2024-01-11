<template>
  <div>
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