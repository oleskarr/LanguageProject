<template>
    <div class="p-4 bg-green-100 rounded-lg relative">
      <textarea v-if="isEditable" v-model="modelValue" class="w-full p-2 bg-transparent border-none outline-none"></textarea>
      <p v-else>{{ modelValue }}</p>
      <button class="absolute top-2 right-2 text-sm" @click="copyText">Копировать</button>
    </div>
  </template>
  
  <script setup>
  defineProps({
    modelValue: String,
    isEditable: { type: Boolean, default: false }
  });
  
  const copyText = () => {
    navigator.clipboard.writeText(modelValue);
  };
  </script>
  