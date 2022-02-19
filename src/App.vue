<template>
 <section class="catalog">  <!--Секция каталог товаров-->
        <ul class="catalog__list">  <!--Список товаров-->

          <li class="catalog__item" v-for="(product, index) in products" :key="index">  <!--товар-->
            <a class="catalog__pic" href="#">
              <img :src="product.image"  alt="{{ product.title }}">
            </a>

            <h3 class="catalog__title">
              <a href="#">
                {{ product.title }}
              </a>
            </h3>

            <span class="catalog__price">
              {{ product.price }} ₽
            </span>

            <ul class="colors colors--black">
              <li class="colors__item">
                <label class="colors__label" for='gg'>
                  <input class="colors__radio sr-only" type="radio" name="color-1"
                    value="#73B6EA" checked="" id="gg">
                  <span class="colors__value" style="background-color: #73B6EA;">
                  </span>
                </label>
              </li>
              <li class="colors__item">
                <label class="colors__label"  for="asd">
                  <input class="colors__radio sr-only" type="radio" name="color-1"
                    value="#8BE000" id="asd">
                  <span class="colors__value" style="background-color: #8BE000;">
                  </span>
                </label>
              </li>
              <li class="colors__item">
                <label class="colors__label"  for="qwerty">
                  <input class="colors__radio sr-only" type="radio" name="color-1"
                    value="#222" id="qwerty">
                  <span class="colors__value" style="background-color: #222;">
                  </span>
                </label>
              </li>
            </ul>
          </li>
        </ul>

        <ul class="catalog__pagination pagination"><!--Слайдер ...  На   след. страницу-->
          <li class="pagination__item">
            <a class="pagination__link pagination__link--arrow pagination__link--disabled"
            aria-label="Предыдущая страница">
              <svg width="8" height="14" fill="currentColor">
                <use xlink:href="#icon-arrow-left"></use>
              </svg>
            </a>
          </li>
          <li class="pagination__item">
            <a class="pagination__link pagination__link--current">
              1
            </a>
          </li>
          <li class="pagination__item">
            <a class="pagination__link" href="#">
              2
            </a>
          </li>
          <li class="pagination__item">
            <a class="pagination__link" href="#">
              3
            </a>
          </li>
          <li class="pagination__item">
            <a class="pagination__link" href="#">
              4
            </a>
          </li>
          <li class="pagination__item">
            <a class="pagination__link" href="#">
              ...
            </a>
          </li>
          <li class="pagination__item">
            <a class="pagination__link" href="#">
              10
            </a>
          </li>
          <li class="pagination__item">
            <a class="pagination__link pagination__link--arrow" href="#"
            aria-label="Следующая страница">
              <svg width="8" height="14" fill="currentColor">
                <use xlink:href="#icon-arrow-right"></use>
              </svg>
            </a>
          </li>
        </ul>
      </section>
</template>

<script>
import products from './data/products'; /* Импортируем массив с товарами */

export default {
  name: 'App',
  data() {
    return {
      products,
    };
  },
};
</script>
