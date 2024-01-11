<template>
  <nav class="border-gray-200 bg-transparent">
    <div class="max-w-screen-xl flex flex-wrap items-center md:justify-center justify-end mx-auto p-4">
      <div class="flex md:order-2">
        <button data-collapse-toggle="navbar-search" type="button" class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm rounded-lg md:hidden focus:outline-none focus:ring-2 text-gray-400 hover:bg-neutral-700 focus:ring-gray-600" aria-controls="navbar-search" aria-expanded="false">
          <span class="sr-only">Menu</span>
          <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 1h15M1 7h15M1 13h15"/>
          </svg>
        </button>
      </div>
      <div class="items-center justify-between hidden w-full md:flex md:w-auto md:order-1" id="navbar-search">
        <ul class="flex flex-col p-4 md:p-0 mt-4 font-medium border rounded-lg bg-neutral-50 md:space-x-8 rtl:space-x-reverse md:flex-row md:mt-0 md:border-0 bg-neutral-800 md:bg-neutral-900 border-gray-700">
          <li>
            <router-link to="/" class="block py-2 px-3 text-white bg-neutral-800 rounded md:bg-transparent md:p-0 hover:bg-white hover:text-neutral-800">Inicio</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
