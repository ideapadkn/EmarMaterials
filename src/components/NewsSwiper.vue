<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
// import { Pagination } from 'swiper'
import 'swiper/css'
import 'swiper/css/pagination'
import { ref } from 'vue';

const newProducts = ref([
  {
    img: '../assest/img/new/1.png',
    type: 'Новинки',
    title: 'Корзина центральная с организацией 664-764мм Muller',
    review: 20,
    rating: 4.5,
    salePrice: '4 000 740 so‘m',
    price: '4 200 740 so‘m',
    id: 1,
  },
  {
    img: '../assest/img/new/2.png',
    type: 'Новинки',
    title: 'Відро Gemini 16л сіре Muller',
    review: 7,
    rating: 4.3,
    salePrice: '450 000 so‘m',
    // price: '4 200 740 so‘m',
    id: 2,
  },
  {
    img: '../assest/img/new/3.png',
    type: 'Новинки',
    title: 'Мусорниця Taurus 40 1x16 + 1x8л сіра',
    review: 12,
    rating: 4.1,
    salePrice: '1 500 000 so‘m',
    // price: '4 200 740 so‘m',
    id: 3,
  },
  {
    img: '../assest/img/new/3.png',
    type: 'Новинки',
    title: 'Кошик центральний раттан 764-864мм Muller',
    review: 4,
    rating: 4.5,
    salePrice: '800 740 so‘m',
    // price: '4 200 740 so‘m',
    id: 4,
  },
  {
    img: '../assest/img/new/3.png',
    type: 'Новинки',
    title: 'Корзина центральная с организацией 664-764мм Muller',
    review: 20,
    rating: 4.5,
    salePrice: '4 000 740 so‘m',
    price: '4 200 740 so‘m',
    id: 5,
  },
  {
    img: '../assest/img/new/3.png',
    type: 'Новинки',
    title: 'Кошик центральний раттан 764-864мм Muller',
    review: 4,
    rating: 4.5,
    salePrice: '4 000 740 so‘m',
    // price: '4 200 740 so‘m',
    id: 6,
  },
])

</script>

<template>
  <div class="news-blog-swiper">
    <h2 class="news-blog__title mb-4">Новинки</h2>
    <Swiper :space-between="20" :slides-per-view="4" :loop="true" :pagination="true" :show="4" :autoplay="{
      delay: 3000,
      disableOnInteraction: false,
      pauseOnMouseEnter: true
    }">
      <Swiper-slide v-for="newProduct in newProducts" :key="newProduct.id">
        <router-link class="flex gap-5" to="/">
          <div class="w-[330px] h-[564px] flex flex-col justify-between p-4 bg-white rounded cursor-pointer">
            <img class="mb-4 w-[298px] h-[250px] bg-slate-300" :src="newProduct.img" :alt="newProduct.id">
            <div class="product-info flex flex-col gap-3">
              <h2 class="product-info__title">{{ newProduct.title }}</h2>
              <div class="product-info__review flex gap-4">
                <p class="flex gap-1">
                  <img src="../assets/img/new/review.svg" alt="review">
                  <span>{{ newProduct.review }} отзывов</span>
                </p>
                <p class="flex gap-1">
                  <img src="../assets/img/new/star.svg" alt="star">
                  <span>{{ newProduct.rating }}</span>
                </p>
              </div>
              <p class="product-info__prices">
                {{ newProduct.salePrice }}
                <span>{{ newProduct.price }}</span>
              </p>
            </div>
            <div class="news-blog-btns flex gap-[10px]">
              <button class="news-blog__btn flex items-center">
                <img src="../assets/img/icons/shoppingBtn.svg" alt="shopping">
                Корзина
              </button>
              <button class="news-blog__click">
                <img src="../assets/img/icons/comparison.svg" alt="comparison">
              </button>
              <button class="news-blog__click">
                <img src="../assets/img/icons/heart.svg" alt="heart">
              </button>
            </div>
          </div>
        </router-link>
      </Swiper-slide>
    </Swiper>
  </div>
</template>

<style lang="scss" scoped>
.news-blog-swiper {
  .news-blog__title {
    color: #212121;
    font-size: 32px;
    font-weight: 450;
  }

  .swiper {
    max-width: 1380px;

    .product-info {
      .product-info__title {
        color: #212121;
        font-size: 22px;
        font-weight: 450;
        transition: all .4s;

        &:hover {
          color: #068C53;
        }
      }

      .product-info__review {
        p {
          color: #898989;
          font-size: 21px;
          font-weight: 450;
        }
      }

      .product-info__prices {
        color: #212121;
        font-size: 30px;
        font-weight: 500;
        margin-bottom: 16px;

        span {
          display: block;
          color: #898989;
          font-size: 22px;
          font-weight: 450;
          text-decoration-line: line-through;
        }
      }
    }

    .news-blog-btns {
      .news-blog__btn {
        padding: 12px 34px;
        border-radius: 4px;
        background: #068C53;
        color: #FFF;
        font-size: 22px;
        font-weight: 450;
        transition: all .4s;

        &:hover {
          background-color: #067244;
        }
      }

      .news-blog__click {
        border-radius: 4px;
        background: rgba(6, 140, 83, 0.08);
        padding: 13px;
        transition: all .4s;

        &:hover {
          background: rgba(3, 70, 41, 0.1);
        }
      }
    }
  }
}
</style>