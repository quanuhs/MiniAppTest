<template>
    <div class="progress-bar">
      <div class="progress-bar-inner" :style="{ width: progress+'%' }"></div>
    </div>
  </template>

  
  
  <script setup>
  import { defineProps, computed } from 'vue'

  
  const props = defineProps({
    progress: Number
  })

  </script>
  
  <style scoped>
  
  .progress-bar {
    width: 100%;
    height: 6px;
    position: relative;
    border-radius: 20px;
    background: var(--gray-100);
  }

  .progress-bar-inner {
    height: 100%;
    width: 0%; /* Эта ширина будет динамически изменяться */
    position: absolute;
    border-radius: 20px;
    background: var(--accent-color);
  }

  </style>
  