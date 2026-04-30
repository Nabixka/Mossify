<script setup>
import Home from './components/Home.vue';
import { Icon } from '@iconify/vue';
import Shop from './components/Shop.vue';

</script>

<template>
  <div class="bg-linear-to-b from-gray-100/70 to-gray-200/50 min-h-screen pb-10">
    <nav class="bg-white p-3 flex justify-between">
      <Icon icon="ci:hamburger-lg" width="27" height="27" />
      <div>
        <h3>Mossify</h3>
      </div>
      <Icon icon="mdi:cart" width="24" height="24" />
    </nav>

    <!-- <Home /> -->
    <!-- <Shop /> -->
  </div>
</template>
