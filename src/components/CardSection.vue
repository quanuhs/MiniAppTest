<template>
  <section class="card-section">
    <div class="container">
      <div class="cards-wrapper">
        <Card
          :imageSrc="zhepaImg"
          title="Готовы ли вы к новому?"
          questionCount="21 вопрос"
        />
        <Card
          :imageSrc="heartImg"
          title="Ваша совместимость"
          questionCount="15 вопросов"
        />
        <Card
          :imageSrc="zhepaImg"
          title="Расскажите, о чём мечтаете"
          questionCount="13 вопросов"
        />
        <Card
          :imageSrc="heartImg"
          title="Поделитесь сокровенным"
          questionCount="25 вопросов"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import zhepaImg from '@/assets/img/zhepa.svg'
import heartImg from '@/assets/img/heart.svg'
import Card from './Card.vue'
</script>

<style scoped>
.card-section {
  margin: 20px;
}

.cards-wrapper {
  display: grid;
  gap: 15px;
  padding: 15px;
}

.cards-wrapper.even {
  grid-template-columns: repeat(2, 1fr);
}

.cards-wrapper.odd {
  grid-template-columns: repeat(3, 1fr);
}

</style>
