<script setup>
import { ref } from "vue";
const feedbacks = ref([
  {
    title: 'Обратный звонок менеджера',
    img: '../assets/feedback/',
    id: 1,
  },
  {
    title: 'Статус заказа',
    img: '../assets/feedback/',
    id: 2,
  },
  {
    title: 'Сроки выполнения работ',
    img: '../assets/feedback/',
    id: 3,
  },
  {
    title: 'Прайс остатков',
    img: '../assets/feedback/',
    id: 4,
  },
  {
    title: 'Загрузки',
    img: '../assets/feedback/',
    id: 5,
  },
  {
    title: 'Маркетинговая поддержка',
    img: '../assets/feedback/',
    id: 6,
  },
  {
    title: 'Оплата и доставка',
    img: '../assets/feedback/',
    id: 7,
  },
  {
    title: 'Гарантии',
    img: '../assets/feedback/',
    id: 8,
  },
])
</script>

<template>
  <div class="mb-10">
    <ul class="feedback">
      <li v-for="feedback in feedbacks" :key="feedback.id" class="feedback-li">
        <router-link class="flex items-center gap-4" to="/">
          <div class="img">
            <img :src="feedback.img" :alt="feedback.id">
          </div>
          {{ feedback.title }}
        </router-link>
      </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.feedback {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;

  &-li {
    width: 330px;
    border-radius: 4px;
    background: #FFF;
    box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.02);
    padding: 20px;
    color: #000;
    font-size: 22px;
    font-weight: 450;
    transition: all .4s;

    &:hover {
      color: #068C53;
    }

    .img {
      display: flex;
      width: 56px;
      height: 56px;
      padding: 8px;
      justify-content: center;
      align-items: center;
      border-radius: 50px;
      background: #F5F5F6;
    }
  }
}
</style>