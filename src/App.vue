<script setup>
import Home from './components/Home.vue';
import { Icon } from '@iconify/vue';
import Shop from './components/Shop.vue';
import Cart from './components/Cart.vue';
import { ref } from 'vue';
import About from './components/About.vue';

const isShow = ref(true)
const handleSection = ref("")

</script>

<template>
  <div class="bg-linear-to-b from-gray-100/70 to-gray-200/50 min-h-screen pb-10">
    <nav class="z-50 bg-white">
      <div class="flex justify-between p-3">
        <button @click="isShow = !isShow">
          <Icon icon="ci:hamburger-lg" width="27" height="27" />
        </button>
        <div>
          <h3>Mossify</h3>
        </div>
        <button @click="handleSection = 'cart'">
          <Icon icon="mdi:cart" width="24" height="24" />
        </button>
      </div>

      <div v-if="isShow" class="bg-gray-200 pl-5 pr-5 pt-7 text-center flex flex-col gap-3 pb-5">
        <h3 class="border border-green-950 py-1 rounded-lg">Home</h3>
        <button @click="handleSection = 'shop', isShow = false" class="border border-green-950 py-1 rounded-lg">Shop</button>
        <button @click="handleSection = 'about', isShow = false" class="border border-green-950 py-1 rounded-lg">About</button>
      </div>
    </nav>

    <section v-if="handleSection === 'cart'">
      <Cart />
    </section>

    <section v-else-if="handleSection === 'shop'">
      <Shop />
    </section>

    <section v-else-if="handleSection === 'about'">
      <About />
    </section>


    <!-- <Home /> -->
  </div>
</template>
