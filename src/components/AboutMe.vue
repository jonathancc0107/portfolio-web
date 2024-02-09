<template>
  <section id="about-me" class="section mx-auto lg:w-[740px] w-full pb-12">
    <h1 class="text-2xl text-white font-bold mb-3">
      <span class="material-icons-outlined align-middle">email</span>
      {{ $t('home.aboutMe.title') }}
    </h1>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
      <div class="col-span-1 md:col-span-2 order-2 md:order-1">
        <p class="text-white mb-4"> {{ $t('home.aboutMe.text_1') }} </p>
        <p class="text-white"> {{ $t('home.aboutMe.text_2') }} </p>
      </div>
      <div class="order-1 md:order-2">
        <img class="rounded-lg h-auto shadow-xl shadow-gray-800" src="../assets/img/Pfp.jpg" alt="photo-main">
      </div>
    </div>
  </section>
</template>