<template>
 <section class="catalog">  <!--Секция каталог товаров-->

        <ProductList :products="products"/> <!--Компонент со списком  товаров-->
        <ProductList :products="products"/>    <!--Компонент со списком  товаров-->

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
import ProductList from './components/ProductList.vue';/* Импортируем компонент  */

export default {
  name: 'App',
  components: { ProductList },
  data() {
    return {
      products,
    };
  },
};
</script>
