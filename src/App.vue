<script setup>
import Modal from "@/components/Modal.vue";
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
import {ref} from "vue";

let isOpen = ref(false);
</script>

<template>
  <div class="page-wrapper">
    <Header @toggleModal="isOpen = !isOpen" />

    <main class="main">
      <router-view></router-view>
    </main>

    <Footer/>
    <Modal :isOpen="isOpen" @toggleModal="isOpen = !isOpen" />
  </div>
</template>

<style scoped>

</style>
