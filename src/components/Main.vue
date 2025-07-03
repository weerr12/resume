<script setup lang="ts">
import { Download } from "lucide-vue-next";
</script>

<template>
  <div class="flex flex-col gap-2 text-center lg:text-left">
    <h2 class="text-2xl sm:text-3xl font-semibold dark:text-gray-300">
      Werasak Mayer
    </h2>
    <h4
      class="font-medium text-xl sm:text-2xl text-blue-600 dark:text-blue-400"
    >
      Frontend Developer
    </h4>
    <div class="mt-2">
      <p class="text-sm sm:text-base text-gray-600 dark:text-gray-300">
        I build accessible, pixel-perfect digital
      </p>
      <p class="text-sm sm:text-base text-gray-600 dark:text-gray-300">
        experiences for the web.
      </p>
    </div>
    <span>
      <a href="resume.pdf" download target="_blank">
        <span
          class="inline-flex download items-center gap-2 sm:gap-4 justify-center w-full sm:w-48 h-10 px-4 sm:px-6 py-2 mt-4 text-sm sm:text-base font-medium text-white bg-blue-600 rounded-lg shadow-md hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2"
        >
          View Resume
          <Download class="w-4 h-4 download" />
        </span>
      </a>
    </span>
  </div>
</template>
