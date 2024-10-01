<script setup>
import { ref, computed } from 'vue';

const state = ref({ isNavShow: false });

const navClass = computed(() =>
  state.isNavShow ? 'collapse navbar-collapse show' : 'collapse navbar-collapse'
);

const toggleshow = () => (state.isNavShow = !state.isNavShow);
</script>

<template>
  <nav class="header sticky-top shadow">
    <div class="container-fluid">
      <router-link class="navbar-brand" to="/">
        <div class="Logo" style="font-weight: bold">styleshop</div>
      </router-link>
      <button
        class="navber-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#collapsibleNavbar"
        @click="toggleshow"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div :class="navClass" id="collapsibleNavbar" style="flex-grow: 0">
        <div style="flex-direction: row; display: flex">
          <router-link to="/top">상의</router-link>
          <router-link to="/bottom">하의</router-link>
        </div>
      </div>
    </div>
  </nav>
</template>

<style setup>
.shadow {
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.01);
}
</style>
