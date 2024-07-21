<template>
    <form class="form" @submit.prevent="handleSubmit">
      <div class="answer-container">
        <h3 class="question-title">{{ questionTitle }}</h3>
        <div class="answers-wrapper">
          <div v-for="(answer, index) in answers" :key="index" class="answer">
            <input type="checkbox" class="checkbox__input" :id="answer.value" :value="answer.value" v-model="selectedAnswers">
            <label :for="answer.value" class="checkbox__name">{{ answer.text }}</label>
          </div>
        </div>
      </div>
      <div class="answer__buttons">
        <button type="submit" class="answer__submit">Далее</button>
        <button type="button" class="answer__skip" @click="handleSkip">Не хочу отвечать</button>
      </div>
    </form>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const props = defineProps({
    questionTitle: String,
    answers: Array
  })
  
  const selectedAnswers = ref([])
  
  const handleSubmit = () => {
    // Логика отправки формы
  }
  
  const handleSkip = () => {
    // Логика пропуска вопроса
  }
  </script>
  
  <style scoped>
  .form {
    display: flex;
    padding: 20px;
    flex-direction: column;
    align-items: center;
    justify-content: end;
    align-self: stretch;
    gap: 32px;
    border-top-right-radius: 20px;
    border-top-left-radius: 20px;
    background: var(--gray-300);
  }
  
  .answer-container {
    display: flex;
    flex-direction: column;
    align-self: stretch;
    gap: 24px;
  }
  
  .question-title {
    text-align: center;
  }
  
  .answers-wrapper {
    display: flex;
    flex-direction: column;
    justify-self: stretch;
    gap: 8px;
  }
  
  .checkbox__name {
    display: flex;
    padding: 15px 20px;
    width: 100%;
    justify-content: space-between;
    align-items: center;
    align-self: stretch;
    outline: none;
    border-radius: 10px;
    background: var(--gray-200);
  }
  
  .checkbox__input {
    position: absolute;
    z-index: -1;
    opacity: 0;
  }
  
  .checkbox__input+label {
    display: flex;
    align-items: center;
    width: 100%;
  }
  
  .checkbox__input+label::after {
    content: '';
    display: inline-block;
    width: 20px;
    height: 20px;
    margin-left: auto;
    background-color: var(--gray-100);
    border-radius: 20px;
    background-repeat: no-repeat;
    background-position: center center;
    background-size: 9px 8px;
  }
  
  .checkbox__input:checked+label::after {
    background-image: url(@/assets/img/checked.svg);
    background-color: var(--accent-color);
  }
  
  .checkbox__input:checked+label {
    outline: 2px solid var(--accent-color);
    outline-offset: -2px;
  }
  
  .answer__buttons {
    display: flex;
    flex-direction: column;
    align-self: stretch;
  }
  
  .answer__submit {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 10px;
    font-size: 14px;
    font-family: Inter;
    font-weight: 600;
    border: none;
    border-radius: 40px;
    color: var(--white);
    background: var(--gray-100);
  }
  
  .answer__skip {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 10px;
    font-size: 14px;
    font-family: Inter;
    font-weight: 400;
    border: none;
    color: var(--secondary-text);
    background-color: rgba(0, 0, 0, 0);
  }
  </style>
  