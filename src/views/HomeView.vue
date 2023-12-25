<template>
  <section class="banner">
    <div class="container">
      <div class="banner-item">
        <h2 class="banner-item__title">Онлайн-сервис доставки еды на дом</h2>

        <p class="banner-item__subtitle">Блюда из любимого ресторана привезет курьер в перчатках, маске и с
          антисептиком</p>
      </div>
    </div>
  </section>

  <section class="products">
    <div class="container">
      <div class="products-header">
        <h3 class="products-header__title">Рестораны</h3>

        <input class="products-header__search" type="search" placeholder="Поиск блюд и ресторанов">
      </div>

      <div id="rests-container" class="products-wrapper">
        <router-link
            class="products-card"
            v-for="rest in restsArray"
            :key="rest.id"
            :to="`./rest?id=${rest.id}`"
        >
          <div class="products-card__image">
            <img :src="getUrl(rest.image)" :alt=rest.title>
          </div>

          <div class="products-card__description">
            <div class="products-card__description-row">
              <h4 class="products-card__description-title">{{ rest.title }}</h4>
              <div class="products-card__description-badge">{{ rest.time }}&nbsp;мин</div>
            </div>

            <div class="products-card__description-row">
              <div class="products-card__description-info">
                <div class="products-card__description-rating">
                  <img src="../assets/img/icons/star.svg" alt="rating star image">
                  <span>{{ rest.rating }}</span>
                </div>
                <div class="products-card__description-price">От {{ rest.price }}&nbsp;₽</div>
                <div class="products-card__description-group">{{ rest.type }}</div>
              </div>
            </div>
          </div>
        </router-link>
      </div>
    </div>
  </section>
</template>

<script setup>
import {restsArray} from "@/constants/rests.js";

const getUrl = (name) => {
  return new URL(`../assets/img/rests/${name}`, import.meta.url);
}
</script>
