<script setup>
import Header from './Header.vue';
// import Footer from './Footer.vue';
</script>

<template>
  <div class="fauid-container">
    <Header />
    <div class="content">
      <slot></slot>
    </div>
    <!-- <Footer /> -->
  </div>
</template>
