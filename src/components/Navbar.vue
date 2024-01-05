<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
  <div class="navbar flex">
    <nav class="navbar-header bg-[#323436] w-full">
      <div class="main-container flex justify-between">
        <div class="flex gap-8 items-center">
          <p class="nav-text">
            <img class="svg inline-block mr-[6px]" src="../assets/img/icons/pin.svg" alt="pin">
            Tashkent
          </p>
          <p class="nav-text">
            <img class="svg inline-block mr-[6px]" src="../assets/img/icons/lang.svg" alt="lang">
            Rus
          </p>
          <p class="nav-text">
            <img class="svg inline-block mr-[6px]" src="../assets/img/icons/phone.svg" alt="phone">
            +9998 71 228-20-87<span class="ml-[6px] opacity-60">(время работы с 06:00 до 20:00)</span>
          </p>
        </div>
        <div class="navbar-menu">
          <ul class="flex gap-8">
            <li class="menu-text">
              <router-link to="/about">О компании</router-link>
            </li>
            <li class="menu-text">
              <router-link to="/">Партнерам</router-link>
            </li>
            <li class="menu-text">
              <router-link to="/guarantee">Гарантии</router-link>
            </li>
            <li class="menu-text">
              <router-link to="/">Оплата и доставка</router-link>
            </li>
            <li class="menu-text">
              <router-link to="/">Трудоустройство</router-link>
            </li>
            <li class="menu-text">
              <router-link to="/">Контакты</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <div>

    </div>
  </div>
</template>

<style lang="scss" scoped>
.navbar {
  &-header {
    padding: 14px 0;

    .nav-text {
      display: flex;
      align-items: center;
      color: #FFF;
      font-size: 20px;
      font-style: normal;
      font-weight: 500;
      line-height: normal;
    }

    .navbar-menu {
      ul {
        .menu-text {
          color: #FFF;
          font-size: 20px;
          font-style: normal;
          font-weight: 450;
          line-height: normal;
        }
      }
    }
  }
}
</style>