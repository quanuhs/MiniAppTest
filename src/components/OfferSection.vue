<template>
  <section>
    <div class="container">
      <div class="offer-wrapper">
        <h1 class="offer-title">Пройдите вместе короткие тесты и узнайте друг друга</h1>
        <img src="@/assets/img/procents.svg" alt="procents" class="offer__image" />
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>


.offer-wrapper {
  display: flex;
  justify-content: end;
  align-items: center;
  height: 162px;
  padding: 0 20px 0 130px;
  position: relative;
  overflow: hidden;
  border-radius: 10px;
  background: var(--accent-color);
}

.offer-title {
  flex: 100;
  font-size: 16px;
  font-weight: 400;
  color: var(--white);
}

.offer__image {
  width: 118px;
  height: 118px;
  transform: rotate(14deg);
  flex-shrink: 0;
  position: absolute;
  left: -25px;
  bottom: 24px;
  border-radius: 10px;
  background: #171923;
  box-shadow: 0px 0px 594.72px 0px #C882D3, 0px 0px 339.84px 0px #C882D3, 0px 0px 198.24px 0px #C882D3, 0px 0px 99.12px 0px #C882D3, 0px 0px 28.32px 0px #C882D3, 0px 0px 14.16px 0px #C882D3;
}
</style>
