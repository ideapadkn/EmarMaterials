<script setup>

</script>

<template>
  <div class="sale bg-white rounded-md w-[360px] p-4 mt-5">
    <h2 class="sale-title">Распродажа</h2>
    <div class="line bg-[#E1E1E1] h-[1px] mt-4 mb-4"></div>
    <div>
      <div class="sale-item flex gap-4">
        <img src="../assets/img/sale/1.png" alt="1">
        <div class="sale-item__info">
          <h4>Мусорница Taurus</h4>
          <p class="sale-price">1 000 510 so‘m</p>
          <p class="price">1 200 510 so‘m</p>
        </div>
      </div>
      <div class="sale-item flex gap-4">
        <img src="../assets/img/sale/2.png" alt="1">
        <div class="sale-item__info">
          <h4>Стул кухонный Pudra</h4>
          <p class="sale-price">800 000 so‘m</p>
          <p class="price">900 000 so‘m</p>
        </div>
      </div>
      <div class="sale-item flex gap-4">
        <img src="../assets/img/sale/3.png" alt="1">
        <div class="sale-item__info">
          <h4>Смеситель ICO 915</h4>
          <p class="sale-price">440 000 so‘m</p>
          <p class="price">500 000 so‘m</p>
        </div>
      </div>
      <div class="sale-item flex gap-4">
        <img src="../assets/img/sale/4.png" alt="1">
        <div class="sale-item__info">
          <h4>Ведро Gemini 16л</h4>
          <p class="sale-price">250 740 so‘m</p>
          <p class="price">300 740 so‘m</p>
        </div>
      </div>
      <button class="sale-btn">
        <router-link to="/">
          Увидеть все
        </router-link>
      </button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.sale {
  &-title {
    color: #212121;
    font-size: 28px;
    font-style: normal;
    font-weight: 450;
    line-height: normal;
  }

  &-item {
    margin-bottom: 21px;

    &__info {
      h4 {
        color: #212121;
        font-size: 20px;
        font-style: normal;
        font-weight: 450;
        line-height: normal;
        margin-bottom: 12px;
      }

      .sale-price {
        color: #068C53;
        font-size: 24px;
        font-style: normal;
        font-weight: 500;
        line-height: normal;
      }

      .price {
        color: #898989;
        font-size: 20px;
        font-style: normal;
        font-weight: 450;
        line-height: normal;
        text-decoration-line: line-through;
      }
    }
  }

  .sale-btn {
    padding: 12px 103px;
    text-align: center;
    color: #068C53;
    font-size: 22px;
    font-style: normal;
    font-weight: 450;
    line-height: normal;
    border-radius: 4px;
    border: 1px solid #E1E1E1;
    background: #FFF;
    transition: all .4s;

    &:hover {
      background-color: #067244;
      color: #fff;
    }
  }
}
</style>