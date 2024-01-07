<script setup>
import { ref } from 'vue';

const navigations = ref([
  {
    icon: '../assets/img/icons/square.svg',
    title: 'Плитные материалы',
    id: 1,
  },
  {
    icon: '../assets/img/icons/square.svg',
    title: 'Мебельная фурнитура',
    id: 2,
  },
  {
    icon: '../assets/img/icons/square.svg',
    title: 'Столешницы и стенпанели',
    id: 3,
  },
  {
    icon: '../assets/img/icons/square.svg',
    title: 'Фасады',
    id: 4,
  },
  {
    icon: '../assets/img/icons/square.svg',
    title: 'Дверные и гардеробные системы',
    id: 5,
  },
  {
    icon: '../assets/img/icons/square.svg',
    title: 'Мебель',
    id: 6,
  },
  {
    icon: '../assets/img/icons/square.svg',
    title: 'Освещение для мебели',
    id: 7,
  },
  {
    icon: '../assets/img/icons/square.svg',
    title: 'Бытовая техника',
    id: 8,
  },
  {
    icon: '../assets/img/icons/square.svg',
    title: 'Изделия из камня',
    id: 9,
  },
  {
    icon: '../assets/img/icons/square.svg',
    title: 'Изделия из метала',
    id: 10,
  },
  {
    icon: '../assets/img/icons/square.svg',
    title: 'Напольные покрытия',
    id: 11,
  },
  {
    icon: '../assets/img/icons/square.svg',
    title: 'Инструменты и расходные материалы',
    id: 12,
  },
  {
    icon: '../assets/img/icons/square.svg',
    title: 'Производственные услуги',
    id: 13,
  },
])
</script>

<template>
  <div class="navigation-menu bg-white rounded-md w-[360px] p-4">
    <ul class="flex flex-col gap-6">
      <li v-for="navigation in navigations" :key="navigation.id">
        <router-link class="flex items-center gap-3" to="/">
          <img :src="navigation.icon" :alt="navigation.id">
          {{ navigation.title }}
        </router-link>
      </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.navigation-menu {
  ul {
    li {
      color: #212121;
      font-size: 22px;
      font-style: normal;
      font-weight: 450;
      line-height: normal;

      router-link {
        display: flex;
      }
    }
  }
}
</style>