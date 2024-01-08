<script setup>
import { RouterLink } from 'vue-router';
import { ref } from 'vue';

const openMenu = ref(false)

const activeMenu = () => {
  openMenu.value = !openMenu.value
  console.log(openMenu.value);
}
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
          <div @click="activeMenu" class="burger-menu">
            <svg xmlns="http://www.w3.org/2000/svg" width="40px" height="40px" viewBox="0 0 24 24" fill="#fff">
              <path d="M20 7L4 7" stroke="#fff" stroke-width="1.5" stroke-linecap="round" />
              <path opacity="0.5" d="M20 12L4 12" stroke="#fff" stroke-width="1.5" stroke-linecap="round" />
              <path d="M20 17L4 17" stroke="#fff" stroke-width="1.5" stroke-linecap="round" />
            </svg>
          </div>
          <ul :class="{ open: openMenu }" class="flex gap-8">
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
                <img src="../assets/img/icons/comparison.svg" alt="comparison">
                <p>Сравнение</p>
              </router-link>
            </li>
            <li>
              <router-link class="flex flex-col items-center" to="/">
                <img src="../assets/img/icons/heart.svg" alt="heart">
                <p>Избранное</p>
              </router-link>
            </li>
            <li>
              <router-link class="flex flex-col items-center" to="/">
                <img src="../assets/img/icons/shopping.svg" alt="shopping">
                <p>Корзина</p>
              </router-link>
            </li>
            <li>
              <router-link class="flex flex-col items-center" to="/">
                <img src="../assets/img/icons/user.svg" alt="user">
                <p>Войти</p>
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


    div {
      @media (max-width: 1235px) {
        gap: 0 10px;
      }
    }

    .nav-text {
      display: flex;
      align-items: center;
      color: #FFF;
      font-size: 20px;
      font-style: normal;
      font-weight: 500;
      line-height: normal;

      @media (max-width: 1536px) {
        font-size: 16px;
      }

      @media (max-width: 415px) {
        font-size: 14px;
      }

      span {
        @media (max-width: 1536px) {
          display: none;
        }
      }
    }

    .navbar-menu {
      .burger-menu {
        display: none;

        @media (max-width: 995px) {
          display: block;
        }
      }

      .open {
        width: 200px;
        height: 220px;
        padding: 25px;
        position: fixed;
        right: 0;
        top: 7%;
        display: flex;
        justify-content: space-between;
        flex-direction: column;
        background-color: #323436;
        z-index: 10;
        transition: all 1s;

        li {
          margin-bottom: 5px;
        }
      }

      ul {
        @media (max-width: 1645px) {
          gap: 0 10px;
        }

        @media (max-width: 995px) {
          display: none;
        }

        .menu-text {
          color: #FFF;
          font-size: 20px;
          font-weight: 450;

          @media (max-width: 1536px) {
            font-size: 16px;
          }
        }
      }

    }
  }

  &-main {
    .main-container {
      justify-content: space-between;
      @media (max-width: 1645px) {
        gap: 0 30px;
      }

      @media (max-width: 995px) {
        flex-wrap: wrap;
        gap: 15px;
      }

      .search {
        @media (max-width: 995px) {
          order: 3;
          width: 100%;
        }


        .catalog-btn {
          padding: 14px 32px;
          color: #FFF;
          font-size: 22px;
          font-weight: 450;
          transition: all .4s;

          @media (max-width: 1535px) {
            padding: 10px 26px;
          }

          @media (max-width: 1405px) {
            font-size: 18px;
          }

          @media (max-width: 740px) {
            padding: 5px 10px;
          }
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

            @media (max-width: 1645px) {
              width: 500px;
            }

            @media (max-width: 1535px) {
              width: 400px;
            }

            @media (max-width: 1405px) {
              height: 50px;
            }

            @media (max-width: 995px) {
              width: calc(100vw - 190px);
            }

            @media (max-width: 740px) {
              height: 40px;
              width: calc(100vw - 160px);
            }


            &:focus {
              color: #212121;
            }
          }

          .search-icon {
            position: absolute;
            top: 15px;
            left: 10px;

            @media (max-width: 740px) {
              top: 9px;
            }
          }

          .search-btn {
            padding: 10px 22px;
            color: #FFF;
            font-size: 22px;
            font-weight: 450;
            position: absolute;
            right: 2px;
            top: 2px;
            transition: all .4s;

            @media (max-width: 1405px) {
              font-size: 18px;
            }

            @media (max-width: 592px) {
              display: none;
            }

            @media (max-width: 740px) {
              padding: 5px 10px;
            }
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

            @media (max-width: 1300px) {
              p {
                display: none;
              }
            }

          }
        }
      }
    }
  }
}
</style>