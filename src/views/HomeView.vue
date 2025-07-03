<script setup lang="ts">
import { Sun, Moon } from "lucide-vue-next";
import { useDark, useToggle } from "@vueuse/core";
import { ref, onMounted, onUnmounted, computed } from "vue";
import CustomParticles from "../components/CustomParticles.vue";
import Main from "../components/Main.vue";
import Nav from "../components/Nav.vue";
import Link from "../components/Link.vue";
import About from "../components/About.vue";
import Experience from "../components/Experience.vue";
import Project from "../components/Project.vue";
import Contact from "../components/Contact.vue";

const isDark = useDark();
const toggleDark = useToggle(isDark);

const activeSection = ref("about");

const sections = ["about", "experience", "projects", "contact"];

const updateActiveSection = () => {
  const scrollPosition = window.scrollY;
  const windowHeight = window.innerHeight;
  const documentHeight = document.documentElement.scrollHeight;

  if (scrollPosition + windowHeight >= documentHeight - 50) {
    activeSection.value = "contact";
    return;
  }

  let currentSection = "about";

  for (const sectionId of sections) {
    const section = document.getElementById(sectionId);
    if (section) {
      const rect = section.getBoundingClientRect();
      const sectionTop = rect.top + scrollPosition;
      const sectionHeight = rect.height;
      const sectionCenter = sectionTop + sectionHeight / 2;
      const viewportCenter = scrollPosition + windowHeight / 2;

      if (sectionCenter <= viewportCenter + 100) {
        currentSection = sectionId;
      }
    }
  }

  activeSection.value = currentSection;
};

onMounted(() => {
  window.addEventListener("scroll", updateActiveSection);
  updateActiveSection();
});

onUnmounted(() => {
  window.removeEventListener("scroll", updateActiveSection);
});
</script>

<template>
  <div
    class="min-h-screen bg-gradient-to-br from-white via-blue-50 to-slate-100 dark:from-gray-900 dark:via-gray-800 dark:to-gray-900"
  >
    <CustomParticles class="z-0" />
    <button
      @click="toggleDark()"
      class="fixed top-6 right-6 z-50 inline-flex items-center justify-center w-12 h-12 text-gray-600 bg-white border border-gray-200 rounded-full shadow-lg hover:bg-gray-50 dark:bg-gray-800 dark:border-gray-700 dark:text-gray-300 dark:hover:bg-gray-700 transition-all duration-200 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2"
      :title="isDark ? 'Switch to Light Mode' : 'Switch to Dark Mode'"
    >
      <Sun v-if="isDark" class="w-5 h-5" />
      <Moon v-else class="w-5 h-5" />
    </button>
    <div class="container mx-auto px-6 lg:px-8 py-12 max-w-7xl">
      <div
        class="grid lg:grid-cols-[400px_1fr] gap-12 lg:gap-16 xl:gap-20 min-h-screen items-center"
      >
        <div class="mb-8 lg:mb-0">
          <div
            class="lg:fixed lg:top-14 lg:w-[380px] lg:max-w-lg grid lg:h-screen grid-rows-[auto_auto_auto] lg:grid-rows-[35%_45%_20%] gap-6 lg:gap-0"
          >
            <Main />
            <Nav :activeSection="activeSection" />
            <Link />
          </div>
        </div>

        <div
          class="gap-y-12 sm:gap-y-16 lg:gap-y-24 dark:bg-transparent text-gray-900 dark:text-gray-300 transition-colors duration-300"
        >
          <About />
          <Experience />
          <Project />
          <Contact />
        </div>
      </div>
    </div>
  </div>
</template>
