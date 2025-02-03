<template>
    <div class="container mx-auto p-4">
      <div class="flex justify-between">
        <div class="w-1/2">
          <h2 class="text-xl font-bold">Ваш текст</h2>
          <TextArea v-model="sourceText" :isEditable="true" />
        </div>
        <div class="w-1/2">
          <h2 class="text-xl font-bold">Перевод</h2>
          <TextArea :value="translatedText" />
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref, computed } from "vue";
  import TextArea from "@/components/TextArea.vue";
  
  const sourceText = ref("");
  const translatedText = computed(() => sourceText.value.split("").reverse().join("")); // Заглушка вместо перевода
  </script>
  