<template>
    <div class="progress-count">
      <div class="progress-bar-question">
        <div class="progress-bar-question-inner" :style="{ width: progressWidth }"></div>
      </div>
      <p class="progress-count__text">Ещё {{ remainingQuestions }} вопросов</p>
    </div>
  </template>
  
  <script setup>
  import { defineProps } from 'vue'
  
  const props = defineProps({
    progressWidth: String,
    remainingQuestions: Number
  })
  </script>
  
  <style scoped>
  .progress-count {
    width: 162px;
    display: flex;
    padding: 12px 25px;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    border-radius: 10px;
    background: var(--white);
  }
  
  .progress-bar-question {
    width: 100%;
    height: 6px;
    position: relative;
    border-radius: 20px;
    background: var(--gray-50);
  }
  
  .progress-bar-question-inner {
    height: 100%;
    width: 67%; /* Эта ширина будет динамически изменяться */
    position: absolute;
    border-radius: 20px;
    background: var(--light-accent-color);
  }
  
  .progress-count__text {
    font-size: 12px;
    text-align: center;
    color: var(--gray-300);
  }
  </style>
  