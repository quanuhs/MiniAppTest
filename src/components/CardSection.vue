<template>
  <section class="card-section">
    <div class="container">
      <div class="cards-wrapper">
        <Card
          imageSrc="@/assets/img/zhepa.svg"
          title="Готовы ли вы к новому?"
          questionCount="21 вопрос"
        />
        <Card
          imageSrc="@/assets/img/heart.svg"
          title="Ваша совместимость"
          questionCount="15 вопросов"
        />
        <Card
          imageSrc="@/assets/img/zhepa.svg"
          title="Расскажите, о чём мечтаете"
          questionCount="13 вопросов"
        />
        <Card
          imageSrc="@/assets/img/heart.svg"
          title="Поделитесь сокровенным"
          questionCount="25 вопросов"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import Card from './Card.vue'
</script>

<style scoped>
.card-section {
  margin: 20px;
}

.cards-wrapper {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
}
</style>
