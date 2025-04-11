<script setup>
import blogs from '../data/blogs.json'
</script>

<template>
  <section class="min-h-screen bg-gray-900 text-white py-12 px-4">
    <div class="max-w-6xl mx-auto">
      <h1 class="text-4xl font-extrabold text-center mb-10">📚 Articles</h1>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
            v-for="blog in blogs"
            :key="blog.id"
            class="bg-gray-800 hover:bg-gray-700 transition-colors duration-200 rounded-xl p-6 shadow-md flex flex-col justify-between"
        >
          <div>
            <h2 class="text-xl font-semibold text-blue-400 mb-2 hover:underline cursor-pointer">
              {{ blog.title }}
            </h2>
            <p class="text-sm text-gray-400 mb-3">
              By {{ blog.author }} • {{ blog.date }}
            </p>
            <p class="text-gray-300 text-sm">
              {{ blog.summary }}
            </p>
          </div>
          <div class="mt-4">
            <a href="#" class="text-blue-400 hover:underline text-sm font-medium">Read more →</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
</style>
