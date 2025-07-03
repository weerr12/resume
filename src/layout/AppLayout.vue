<script setup lang="ts">
import Nav from "../components/Nav.vue";
</script>

<template>
  <div>
    <header>
      <Nav />
    </header>
    <main>
      <slot />
    </main>
    <footer>

    </footer>
  </div>
</template>