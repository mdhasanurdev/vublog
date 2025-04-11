<script setup>
import {ref} from 'vue'

const isOpen = ref(false)
const toggleMenu = () => isOpen.value = !isOpen.value
const closeMenu = () => isOpen.value = false
</script>

<template>
  <header class="bg-white shadow-sm dark:bg-gray-900">
    <nav class="max-w-screen-xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
      <RouterLink to="/" class="text-2xl font-bold text-gray-800 dark:text-white hover:text-blue-600 transition">
        VUEBLOG
      </RouterLink>

      <ul class="hidden lg:flex space-x-6 font-medium text-gray-600 dark:text-gray-300">
        <li>
          <RouterLink to="/" class="hover:text-blue-600 transition">Home</RouterLink>
        </li>
        <li>
          <RouterLink to="/about" class="hover:text-blue-600 transition">About</RouterLink>
        </li>
        <li>
          <RouterLink to="/contact" class="hover:text-blue-600 transition">Contact</RouterLink>
        </li>
      </ul>

      <div class="hidden lg:block">
        <a href="#" class="bg-blue-600 hover:bg-blue-700 text-white font-medium py-2 px-4 rounded-lg transition">Get Started</a>
      </div>

      <button @click="toggleMenu" class="lg:hidden text-gray-700 dark:text-gray-300 focus:outline-none">
        <svg v-if="!isOpen" class="w-6 h-6" fill="none" stroke="currentColor" stroke-width="2"
             viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16"/>
        </svg>
        <svg v-else class="w-6 h-6" fill="none" stroke="currentColor" stroke-width="2"
             viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12"/>
        </svg>
      </button>
    </nav>

    <div v-if="isOpen" class="lg:hidden px-4 pb-4 space-y-2">
      <RouterLink to="/" class="block text-gray-700 dark:text-gray-200 hover:text-blue-600 transition py-2" @click="closeMenu">Home</RouterLink>
      <RouterLink to="/about" class="block text-gray-700 dark:text-gray-200 hover:text-blue-600 transition py-2" @click="closeMenu">About</RouterLink>
      <RouterLink to="/contact" class="block text-gray-700 dark:text-gray-200 hover:text-blue-600 transition py-2" @click="closeMenu">Contact</RouterLink>
    </div>
  </header>
</template>

<style scoped>

</style>