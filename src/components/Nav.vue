<script setup lang="ts">
const props = defineProps<{
  activeSection: string;
}>();
</script>

<template>
  <div class="order-3 lg:order-none">
    <nav
      class="flex flex-row items-cemter justify-center lg:flex-col gap-x-2 sm:gap-x-3 lg:gap-x-0 lg:gap-y-4 pb-2 lg:pb-0 overflow-x-auto lg:overflow-x-visible"
    >
      <div class="flex items-center group">
        <span
          :class="[
            'nav-line hidden lg:block',
            activeSection === 'about' ? 'nav-line-active' : 'nav-line-inactive',
          ]"
        ></span>
        <a
          href="#about"
          :class="[
            'py-2 px-1 sm:px-2 rounded-md whitespace-nowrap text-xs sm:text-sm lg:text-base transition-all duration-300 font-medium',
            activeSection === 'about' ? 'nav-text-active' : 'nav-text-inactive',
          ]"
          >ABOUT</a
        >
      </div>
      <div class="flex items-center group">
        <span
          :class="[
            'nav-line hidden lg:block',
            activeSection === 'experience'
              ? 'nav-line-active'
              : 'nav-line-inactive',
          ]"
        ></span>
        <a
          href="#experience"
          :class="[
            'py-2 px-1 sm:px-2 rounded-md whitespace-nowrap text-xs sm:text-sm lg:text-base transition-all duration-300 font-medium',
            activeSection === 'experience'
              ? 'nav-text-active'
              : 'nav-text-inactive',
          ]"
          >EXPERIENCE</a
        >
      </div>
      <div class="flex items-center group">
        <span
          :class="[
            'nav-line hidden lg:block',
            activeSection === 'projects'
              ? 'nav-line-active'
              : 'nav-line-inactive',
          ]"
        ></span>
        <a
          href="#projects"
          :class="[
            'py-2 px-1 sm:px-2 rounded-md whitespace-nowrap text-xs sm:text-sm lg:text-base transition-all duration-300 font-medium',
            activeSection === 'projects'
              ? 'nav-text-active'
              : 'nav-text-inactive',
          ]"
          >PROJECT</a
        >
      </div>
      <div class="flex items-center group">
        <span
          :class="[
            'nav-line hidden lg:block',
            activeSection === 'contact'
              ? 'nav-line-active'
              : 'nav-line-inactive',
          ]"
        ></span>
        <a
          href="#contact"
          :class="[
            'py-2 px-1 sm:px-2 rounded-md whitespace-nowrap text-xs sm:text-sm lg:text-base transition-all duration-300 font-medium',
            activeSection === 'contact'
              ? 'nav-text-active'
              : 'nav-text-inactive',
          ]"
          >CONTACT</a
        >
      </div>
    </nav>
  </div>
</template>
