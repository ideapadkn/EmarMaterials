<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
  <div class="navbar">
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
    <div class="navbar-main bg-white p-[27px]">
      <div class="main-container flex gap-[60px] items-center">
        <div class="logo">
          <img src="../assets/img/logo.png" alt="logo">
        </div>
        <div class="search flex gap-5">
          <button class="catalog-btn rounded bg-[#068C53] hover:bg-[#067244] flex items-center gap-1">
            <img src="../assets/img/icons/app.svg" alt="app">
            Каталог
          </button>
          <div class="search-block">
            <img class="search-icon cursor-pointer" src="../assets/img/icons/search.svg" alt="search">
            <input class="search-input focus:outline-none" type="text" placeholder="Поиск по продуктам">
            <button class="search-btn rounded bg-[#068C53] hover:bg-[#067244]">Поиск</button>
          </div>
        </div>
        <div class="main-menu">
          <ul class="flex gap-4">
            <li>
              <router-link class="flex flex-col items-center" to="/">
                <img src="../assets/img/icons/clock.svg" alt="clock">
                Статус заказа
              </router-link>
            </li>
            <li>
              <router-link class="flex flex-col items-center" to="/">
                <img src="../assets/img/icons/comparison.svg" alt="comparison">
                Сравнение
              </router-link>
            </li>
            <li>
              <router-link class="flex flex-col items-center" to="/">
                <img src="../assets/img/icons/heart.svg" alt="heart">
                Избранное
              </router-link>
            </li>
            <li>
              <router-link class="flex flex-col items-center" to="/">
                <img src="../assets/img/icons/shopping.svg" alt="shopping">
                Корзина
              </router-link>
            </li>
            <li>
              <router-link class="flex flex-col items-center" to="/">
                <img src="../assets/img/icons/user.svg" alt="user">
                Войти
              </router-link>
            </li>
          </ul>
        </div>
      </div>
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
        @media (max-width: 1645px) {
          gap: 0 10px;
        }

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

  &-main {
    .main-container {
      @media (max-width: 1645px) {
        gap: 0 30px;
      }

      .search {
        .catalog-btn {
          padding: 14px 32px;
          color: #FFF;
          font-size: 22px;
          font-style: normal;
          font-weight: 450;
          line-height: normal;
          transition: all .4s;
        }

        &-block {
          position: relative;

          .search-input {
            color: #C1C1C1;
            font-size: 22px;
            font-style: normal;
            font-weight: 400;
            line-height: normal;
            border-radius: 4px;
            border: 1px solid #E1E1E1;
            width: 579px;
            padding: 20px 0px 20px 40px;
            height: 56px;

            &:focus {
              color: #212121;
            }
          }

          .search-icon {
            position: absolute;
            top: 15px;
            left: 10px;
          }

          .search-btn {
            padding: 10px 22px;
            color: #FFF;
            font-size: 22px;
            font-style: normal;
            font-weight: 450;
            line-height: normal;
            position: absolute;
            right: 5px;
            top: 3.3px;
            transition: all .4s;
          }
        }
      }

      .main-menu {
        ul {
          li {
            color: #212121;
            font-size: 20px;
            font-style: normal;
            font-weight: 450;
            line-height: normal;
          }
        }
      }
    }
  }
}
</style>