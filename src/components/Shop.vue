<script setup>
    import { onMounted, ref, inject } from 'vue';
    import { Icon } from '@iconify/vue';

    const { addToCart } = inject('cart')

    const item = ref([
      {
        "nama" : "Kokedama Sirih Gading",
        "harga" : 35000,
        "image" : "/kokedama.jpg"
      },
      {
        "nama" : "Kokedama Lidah Kodok",
        "harga" : 50000,
        "image" : "/kokedama.jpg"
      }
    ])

</script>

<template>
  <div class="flex flex-col gap-2 px-5">
    <!-- Header -->
    <h1 class="font-serif text-3xl text-green-950 font-bold">Shop</h1>
    <h3 class="text-gray-500">Temukan kokedama favoritmu di sini</h3>

    <!-- Grid -->
    <div class="grid lg:grid-cols-5 grid-cols-2 gap-4 pt-8">
      
      <!-- Card -->
      <div v-for="i in item" class="bg-white rounded-2xl overflow-hidden shadow-sm hover:shadow-md transition duration-300">
        <img :src="i.image" class="h-40 w-full object-cover">

        <div class="p-3">
          <h4 class="text-sm font-medium text-gray-800">{{ i.nama }}</h4>
          <h4 class="text-green-900 font-bold mt-1">Rp{{ i.harga }}</h4>

          <button @click="addToCart(i)" class="mt-3 w-full bg-green-900 text-white py-1.5 rounded-lg text-sm hover:bg-green-800 transition">
            + Keranjang
          </button>
        </div>
      </div>

    </div>

    <!-- Custom Section -->
    <div class="bg-gradient-to-r from-green-100 to-green-200 w-full rounded-2xl p-4 mt-8 flex flex-col gap-3 shadow-sm">
      <h3 class="font-serif flex items-center gap-2 font-bold text-green-900 text-lg">
        <Icon icon="meteor-icons:leaf" width="22" height="22"/>
        Custom Kokedama
      </h3>

      <p class="text-sm text-gray-700">
        Buat Kokedama sesuai keinginanmu! Pilih tanaman, ukuran, dan gaya sendiri.
      </p>

      <button class="flex items-center justify-center gap-2 bg-green-900 text-white py-2 rounded-lg text-sm font-medium hover:bg-green-800 transition w-full">
        Pesan Sekarang 
        <Icon icon="maki:arrow" width="14" height="14" />
      </button>
    </div>
  </div>
</template>