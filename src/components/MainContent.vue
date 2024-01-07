<script setup>
import Feedback from './Feedback.vue';
import MainSwiper from './MainSwiper.vue';
import NewsSwiper from './NewsSwiper.vue';
</script>

<template>
  <div>
    <div class="main flex gap-5 mb-10">
      <MainSwiper />
      <div class="flex flex-col gap-5">
        <div class="check-order rounded">
          <h3 class="check-order__title">Готов ли ваш заказ?</h3>
          <p class="check-order__text">А давайте проверим :)</p>
          <button class="check-order__btn">Посмотреть</button>
        </div>
        <div class="eman-studio rounded">
          <h3 class="eman-studio__title">EMAN STUDIO</h3>
          <p class="eman-studio__text">ВЫ МОЖЕТЕ ПОДОБРАТЬ ЦВЕТА ДЛЯ ВАШЕГО
            ИНТЕРЬЕРА НЕ ВЫХОДЯ ИЗ ДОМА!</p>
          <button class="eman-studio__btn flex items-center text-center ">Открыть
            <img src="../assets/img/icons/arrow-right.svg" alt="arrow">
          </button>
        </div>
      </div>
    </div>
    <Feedback />
    <NewsSwiper />
  </div>
</template>

<style lang="scss" scoped>
.check-order {
  background-image: url(../assets/img/slider/bg1.png);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  padding: 27.5px 0;
  text-align: center;
  width: 447px;

  &__title {
    color: #FFF;
    font-size: 32px;
    font-weight: 500;
  }

  &__text {
    color: #FFF;
    font-size: 22px;
    font-weight: 400;
    margin-bottom: 24px;
  }

  &__btn {
    color: #068C53;
    font-size: 22px;
    font-weight: 500;
    padding: 11px 50.5px;
    background-color: #fff;
  }
}

.eman-studio {
  padding: 10px 0;
  background-image: url(../assets/img/slider/bg2.png);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  text-align: center;
  color: #fff;
  width: 447px;

  &__title {
    font-size: 32px;
    font-weight: 500;
  }

  &__text {
    font-size: 22px;
    font-weight: 400;
    text-transform: uppercase;
    margin-bottom: 16px;
  }

  &__btn {
    font-size: 22px;
    font-weight: 500;
  }
}
</style>