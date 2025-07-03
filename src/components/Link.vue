<script setup lang="ts">
import {
  Facebook,
  Instagram,
  Linkedin,
  Github,
} from "lucide-vue-next";
</script>

<template>
  <div
    class="flex items-center justify-center lg:justify-start lg:mb-14 order-2 lg:order-none"
  >
    <div class="flex space-x-4 text-gray-600 dark:text-gray-400">
      <a
        href="https://github.com/weerr12"
        target="_blank"
        class="hover:text-gray-900 hover:scale-120 transition-all duration-200 dark:hover:text-gray-300"
      >
        <Github class="w-5 h-5 sm:w-6 sm:h-6" />
      </a>
      <a
        href="https://www.linkedin.com/in/werasak-mayer-3348a4287/"
        target="_blank"
        class="hover:text-gray-900 hover:scale-120 transition-all duration-200 dark:hover:text-gray-300"
      >
        <Linkedin class="w-5 h-5 sm:w-6 sm:h-6" />
      </a>
      <a
        href="https://www.instagram.com/10.00.00.11/"
        target="_blank"
        class="hover:text-gray-900 hover:scale-120 transition-all duration-200 dark:hover:text-gray-300"
      >
        <Instagram class="w-5 h-5 sm:w-6 sm:h-6" />
      </a>
      <a
        href="https://www.facebook.com/werasak.wee.2024"
        target="_blank"
        class="hover:text-gray-900 hover:scale-120 transition-all duration-200 dark:hover:text-gray-300"
      >
        <Facebook class="w-5 h-5 sm:w-6 sm:h-6" />
      </a>
    </div>
  </div>
</template>
