<script setup lang="ts"></script>

<template>
  <section id="projects" class="mb-12 sm:mb-16 lg:mb-24">
    <h3
      class="text-xl sm:text-2xl font-bold mb-4 sm:mb-6 text-gray-900 dark:text-gray-300"
    >
      Projects
    </h3>
    <div class="space-y-6 sm:space-y-8">
      <div
        class="project bg-gray-50 p-4 sm:p-6 rounded-lg transition-colors duration-300 hover:shadow-lg hover:scale-101 dark:hover:shadow-lg dark:hover:scale-101"
      >
        <h4 class="text-lg sm:text-xl font-semibold mb-2 text-gray-900 project">
          LiveScore
        </h4>
        <p
          class="text-gray-700 mb-4 text-sm sm:text-base leading-relaxed project"
        >
          เว็บไซต์แสดงบอลโดยการ mock data ขึ้นมา ใช้ Vue ในการพัฒนาขึ้นมา
        </p>
        <div class="flex gap-2 project">
          <span
            class="bg-blue-100 text-blue-800 px-2 sm:px-3 py-1 rounded text-xs sm:text-sm vue"
            >Vue</span
          >
        </div>
      </div>

      <div
        class="bg-gray-50 project p-4 sm:p-6 rounded-lg transition-colors duration-300 hover:shadow-lg hover:scale-101 dark:hover:shadow-lg dark:hover:scale-101"
      >
        <h4 class="text-lg project sm:text-xl font-semibold mb-2 text-gray-900">
          Portfolio Website
        </h4>
        <p
          class="text-gray-700 project mb-4 text-sm sm:text-base leading-relaxed"
        >
          เว็บไซต์ Portfolio ส่วนตัวที่แสดงผลงานและทักษะ ออกแบบให้ responsive
          และใช้งานง่าย
        </p>
        <div class="flex flex-wrap gap-2 project">
          <span
            class="bg-blue-100 text-blue-800 px-2 sm:px-3 py-1 rounded text-xs sm:text-sm vue"
            >Vue</span
          >
          <span
            class="bg-teal-100 text-teal-800 px-2 sm:px-3 py-1 rounded text-xs sm:text-sm css"
            >Tailwind CSS</span
          >
          <span
            class="bg-yellow-100 text-yellow-800 px-2 sm:px-3 py-1 rounded text-xs sm:text-sm vite"
            >Vite</span
          >
        </div>
      </div>
    </div>
  </section>
</template>
