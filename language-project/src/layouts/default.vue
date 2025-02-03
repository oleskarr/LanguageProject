<template>
    <div class="min-h-screen flex flex-col">
      <header class="bg-gray-300 p-4 flex justify-between items-center">
        <LanguageSwitcher />
      </header>
  
      <main class="flex-1">
        <slot />
      </main>
  
      <Footer />
    </div>
  </template>
  
  <script setup>
  import LanguageSwitcher from "@/components/LanguageSwitcher.vue";
  import Footer from "@/components/Footer.vue";
  </script>
  