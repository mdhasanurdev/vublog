<script setup>
</script>

<template>
  <section class="min-h-screen bg-white dark:bg-gray-900 flex items-center justify-center px-4">
    <div class="w-full max-w-2xl py-12">
      <h2 class="text-3xl md:text-4xl font-bold text-center text-gray-800 dark:text-white mb-4">Contact Us</h2>
      <p class="text-center text-gray-500 dark:text-gray-400 mb-10">
        Have questions or feedback? We'd love to hear from you.
      </p>

      <form @submit.prevent class="space-y-6">
        <div>
          <label for="email" class="block mb-1 text-sm font-medium text-gray-700 dark:text-gray-300">Email</label>
          <input
              type="email"
              id="email"
              required
              class="w-full px-4 py-2 rounded-md bg-gray-100 border border-gray-300 dark:bg-gray-800 dark:border-gray-600 dark:text-white focus:outline-none focus:ring-2 focus:ring-blue-500"
              placeholder="you@example.com"
          />
        </div>

        <div>
          <label for="subject" class="block mb-1 text-sm font-medium text-gray-700 dark:text-gray-300">Subject</label>
          <input
              type="text"
              id="subject"
              required
              class="w-full px-4 py-2 rounded-md bg-gray-100 border border-gray-300 dark:bg-gray-800 dark:border-gray-600 dark:text-white focus:outline-none focus:ring-2 focus:ring-blue-500"
              placeholder="What’s this about?"
          />
        </div>

        <div>
          <label for="message" class="block mb-1 text-sm font-medium text-gray-700 dark:text-gray-300">Message</label>
          <textarea
              id="message"
              rows="5"
              required
              class="w-full px-4 py-2 rounded-md bg-gray-100 border border-gray-300 dark:bg-gray-800 dark:border-gray-600 dark:text-white focus:outline-none focus:ring-2 focus:ring-blue-500"
              placeholder="Write your message here..."
          ></textarea>
        </div>

        <div class="text-center">
          <button
              type="submit"
              class="bg-blue-600 hover:bg-blue-700 text-white font-medium px-6 py-2 rounded-md transition"
          >
            Send Message
          </button>
        </div>
      </form>
    </div>
  </section>
</template>

<style scoped>
</style>
