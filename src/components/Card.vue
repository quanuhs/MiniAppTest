<template>
  <div class="card">
    <img :src="imageSrc" :alt="title" class="card-image" />
    <div class="card-info-wrapper">
      <h3 class="card-title">{{ title }}</h3>
      <div class="progress">
        <div class="progress-bar">
          <div class="progress-bar-inner"></div>
        </div>
        <p class="count">{{ questionCount }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  imageSrc: String,
  title: String,
  questionCount: String,
})
</script>

<style scoped>
.card {
  height: 240px;
  min-width: 152px;
  padding: 15px;
  display: flex;
  flex-direction: column;
  justify-content: end;
  flex: 100;
  position: relative;
  overflow: hidden;
  border-radius: 10px;
  background: var(--gray-300);
  transition: background 0.3s ease;

  &:hover{
    background: var(--gray-hover);
  }
}

.card-info-wrapper {
  display: flex;
  flex-direction: column;
  gap: 18px;
}

.card-title {
  color: var(--white);
  font-size: 16px;
  font-weight: 400;
}

.card-image {
  position: absolute;
  left: -18px;
  top: -10px;
  transform: rotate(-20deg);
}

.progress {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.progress-bar {
  width: 100%;
  height: 6px;
  position: relative;
  border-radius: 20px;
  background: var(--gray-100);
}

.progress-bar-inner {
  height: 100%;
  width: 0%;
  position: absolute;
  border-radius: 20px;
  background: var(--accent-color);
}

.count {
  text-align: center;
  color: var(--secondary-text);
}
</style>
