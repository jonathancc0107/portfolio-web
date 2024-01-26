<template>
  <section id="hero" class="section mx-auto lg:w-[740px] w-full pb-24">
    <h1 class="text-white text-3xl md:text-4xl lg:text-5xl font-bold flex flex-row gap-x-4 pb-6 lg:pb-10">
      {{ $t('home.hero.title') }} Jonathan 
      <a class="flex items-center justify-center" href="https://www.linkedin.com/in/jonathan-caballero-castillo-086918175/" target="_blank">
        <span class="bg-green-900 text-green-300 text-xs font-medium me-2 px-2.5 py-0.5 rounded">{{ $t('home.hero.available') }}</span>
      </a>
    </h1>
    <button class="text-white border border-gray-300 transition hover:scale-110 hover:bg-white hover:text-gray-700 rounded-full py-2 px-4">
      {{ $t('home.hero.download') }}
      <span class="material-icons-outlined align-middle">file_download</span>
    </button>
  </section>
</template>

