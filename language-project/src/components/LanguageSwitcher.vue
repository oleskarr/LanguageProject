<template>
    <div class="flex items-center gap-4">
      <span :class="{'font-bold': lang === 'ru'}" @click="setLang('ru')">Русский</span>
      <button class="bg-yellow-300 p-2 rounded-full" @click="swapLanguages">⇄</button>
      <span :class="{'font-bold': lang === 'en'}" @click="setLang('en')">Английский</span>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  
  const lang = ref("ru");
  
  const swapLanguages = () => {
    lang.value = lang.value === "ru" ? "en" : "ru";
  };
  
  const setLang = (newLang) => {
    lang.value = newLang;
  };
  </script>
  