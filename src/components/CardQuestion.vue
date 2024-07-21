<template>
    <section class="card-question">
      <div class="container">
        <div class="question-container">
          <ProgressBar :progressWidth="progressWidth" :remainingQuestions="remainingQuestions" />
          <QuestionForm :questionTitle="questionTitle" :answers="answers" />
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import ProgressBar from './ProgressBar.vue'
  import QuestionForm from './QuestionForm.vue'
  
  const progressWidth = '67%' // Пример значения, измените по необходимости
  const remainingQuestions = 19
  const questionTitle = 'Какой вид экспериментов вас привлекает?'
  const answers = [
    { text: 'Новые позы', value: 'new_poses' },
    { text: 'Игры с сенсорной депривацией', value: 'sensor' },
    { text: 'Использование еды', value: 'food' },
    { text: 'Публичные места', value: 'public' },
    { text: 'Игрушки и аксессуары', value: 'toys' }
  ]
  </script>
  
  <style scoped>
  .card-question {
    margin: 0;
    height: 100%;
    width: 100%;
  }
  
  .question-container {
    display: flex;
    flex-direction: column;
    gap: 16px;
    height: 100%;
    width: 100%;
    align-items: center;
    justify-content: end;
  }
  </style>
  