<script setup>
import Header from './Header.vue';
// import Footer from './Footer.vue';
</script>

<template>
  <div>
    <Header />
    <div>
      <slot></slot>
    </div>
    <!-- <Footer /> -->
  </div>
</template>
