<template>
  <section class="card-section">
    <div class="container">
      <div :class="gridClass">
        <Card v-for="card in cards" 
          :imageSrc="card.imageSrc"
          :title="card.title"
          :questionCount="card.questionCount">
        </Card>
      </div>
    </div>
  </section>
</template>

<script setup>
import zhepaImg from '@/assets/img/zhepa.svg'
import heartImg from '@/assets/img/heart.svg'
import Card from './Card.vue'
import { computed } from 'vue'

const cards = [
  { imageSrc: zhepaImg, title: 'Готовы ли вы к новому?', questionCount: '21 вопрос' },
  { imageSrc: heartImg, title: 'Ваша совместимость', questionCount: '15 вопросов' },
  { imageSrc: zhepaImg, title: 'Расскажите, о чём мечтаете', questionCount: '13 вопросов' },
  { imageSrc: heartImg, title: 'Поделитесь сокровенным', questionCount: '25 вопросов' }
]

const gridClass = computed(() => {
  return {
    'cards-wrapper': true,
    even: cards.length % 2 === 0,
    odd: cards.length % 2 !== 0
  }
})
</script>

<style scoped>
.card-section {
  margin: 20px;
}

.cards-wrapper {
  display: grid;
  gap: 15px;
}

.cards-wrapper.even {
  grid-template-columns: repeat(2, 1fr);
}

.cards-wrapper.odd {
  grid-template-columns: repeat(3, 1fr);
}


@media only screen and (max-width: 420px) {
  .cards-wrapper{
    grid-template-columns: repeat(1, 1fr) !important;
  }
}

</style>
