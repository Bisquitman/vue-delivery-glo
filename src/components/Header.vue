<template>
  <header class="header">
    <div class="container">
      <div class="header-box">
        <router-link to="./" class="header-logo logo">
          <img src="../assets/img/logo.svg" alt="Логотип сайта">
        </router-link>

        <div class="header-controls">
          <button class="btn btn-primary" type="button">
            <img src="../assets/img/icons/user.svg">
            Войти
          </button>

          <button class="btn btn-outline" type="button" @click="openModal()">
            <img src="../assets/img/icons/shopping-cart.svg">
            Корзина
          </button>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
  const emit = defineEmits(['toggleModal']);
  const openModal = () => emit('toggleModal');
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  min-height: 124px;
}

.header-box {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.header-controls {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 8px;
}
</style>