<script setup>
import {goodsArray} from "@/constants/goods.js";
import {restsArray} from "@/constants/rests.js";

const getImgUrl = (name) => new URL(`../assets/img/goods/${name}`, import.meta.url);

const id = new URLSearchParams(window.location.search).get('id');
const rest = restsArray[id];
</script>

<template>
  <section class="products">
    <div class="container">
      <div class="products-header products-header_goods">
        <h2 class="products-header__title">{{ rest.title }}</h2>

        <div class="products-card__description-info">
          <div class="products-card__description-rating">
            <img src="../assets/img/icons/star.svg" alt="rating star image">
            <span>{{ rest.rating }}</span>
          </div>
          <div class="products-card__description-price">От {{ rest.price }}&nbsp;₽</div>
          <div class="products-card__description-group">{{ rest.type }}</div>
        </div>
      </div>

      <div id="goods-container" class="products-wrapper">
        <article
          class="products-card"
          v-for="goods in goodsArray"
          :key="goods.id"
        >
          <div class="products-card__image">
            <img :src="getImgUrl(goods.image)" :alt=goods.title>
          </div>

          <div class="products-card__description">
            <div class="products-card__description-row">
              <h3 class="products-card__description-name">{{ goods.title }}</h3>
            </div>

            <div class="products-card__description-row">
              <p class="products-card__description-text">
                {{ goods.description }}
              </p>
            </div>

            <div class="products-card__description-row">
              <div class="products-card__description-controls">
                <button class="btn btn-primary">
                  <span>В корзину</span>
                  <img src="../assets/img/icons/shopping-cart-white.svg" alt="Cart icon">
                </button>

                <p class="products-card__description-controls-price">{{ goods.price }}&nbsp;₽</p>
              </div>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>
