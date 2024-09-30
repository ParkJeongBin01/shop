<script setup>
import { ref, computed } from 'vue';

const state = ref({ isNavShow: false });

const navClass = computed(() =>
  state.isNavShow ? 'collape navbar-collapse show' : 'collape navbar-collapse'
);

const toggleNavShow = () => (state.isNavShow = !state.isNavShow);
</script>

<template>
  <div class="Logo">styleshop</div>
</template>

<style setup></style>
